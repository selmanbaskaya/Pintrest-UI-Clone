<script>
import HomePage from "@/pages/HomePage";

export default {
  components: { HomePage },
  data() {
    return {
      mainItems: [
        { title: "Home", icon: "mdi-view-dashboard" },
        { title: "Recent", icon: "mdi-image" },
        { title: "Following", icon: "mdi-help-box" },
      ],
      insightsItems: [
        {
          title: "Messages",
          icon: "mdi-view-dashboard",
          isNotification: false,
        },
        { title: "Notifications", icon: "mdi-image", isNotification: true },
      ],
    };
  },
};
</script>
i

<template>
  <v-app>
    <v-app-bar height="100" flat app color="white">
      <v-layout align-center>
        <v-flex>
          <v-text-field
            color="grey"
            placeholder="Search"
            class="mt-7"
            flat
            solo-inverted
			prepend-inner-icon="mdi-magnify"
          />
        </v-flex>
        <v-btn class="mx-1 ml-4">
          <v-icon>
            mdi-account
          </v-icon>
        </v-btn>
        <v-btn class="ml-3" dark>
          <v-icon>
            mdi-plus
          </v-icon>
        </v-btn>
      </v-layout>
    </v-app-bar>

    <v-navigation-drawer app permanent>
      <v-list-item>
        <v-list-item-avatar>
          <v-img
            width="10"
            lazy-src="../assets/pinterest.png"
            src="../assets/pinterest.png"
          />
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="title">
            Pintrest
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in mainItems" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <div class="mx-4 subtitle-2 grey--text">Insights</div>
      <v-list dense nav>
        <v-list-item v-for="item in insightsItems" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
          <v-list-item-avatar
            v-if="item.isNotification"
            size="20"
            color="orange"
            class="white--text"
          >
            2
          </v-list-item-avatar>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <home-page />
    </v-main>
  </v-app>
</template>

<style></style>
