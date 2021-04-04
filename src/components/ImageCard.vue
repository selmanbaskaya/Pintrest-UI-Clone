<script>
export default {
  props: ["url", "users"],
};
</script>

<template>
  <v-card flat>
    <v-img class="img-card" :src="url" />
    <v-layout class="pt-3" align-center>
      <v-avatar size="40">
        <v-img :src="users.profileImg" />
      </v-avatar>
      <v-flex class="ml-3">
        <div class="subtitle-2">
          {{ users.name }}
        </div>
        <div class="body-2 grey--text">
          {{ users.job }}
        </div>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<style>
.img-card {
	border-radius: 20px !important;
}
</style>
