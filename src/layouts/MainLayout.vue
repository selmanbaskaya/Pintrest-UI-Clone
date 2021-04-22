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
      <v-card flat>
        <v-img
          src="https://assets.website-files.com/5bff8886c3964a992e90d465/5bff98f85ea7faf86504605e_scenes.gif"
        />
        <v-layout class="pt-5 px-8">
          <v-flex text-center>
            <div class="subtitle-2 blue--text">
              Unlock Business Tools
            </div>
            <div class="caption">
              Hurry Up! Now you can unlock out new business tools at your
              Convenience.
            </div>
          </v-flex>
        </v-layout>
      </v-card>
      <v-layout align-center>
        <v-card elevation="5">
          <v-layout>
            <v-avatar>
              <v-img
                src="https://images.unsplash.com/photo-1610024062303-e355e94c7a8c?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjd8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
              />
            </v-avatar>
            <v-flex class="ml-2">
              <div class="subtitle-2">
                Selman Baskaya
              </div>
              <div class="body-2 greyy--text">Software Engineer</div>
            </v-flex>
          </v-layout>
        </v-card>
      </v-layout>
    </v-navigation-drawer>

    <v-main>
      <home-page />
    </v-main>
  </v-app>
</template>

<style></style>
