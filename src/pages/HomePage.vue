<script>
import { Stack, StackItem } from "vue-stack-grid";
import ImageCard from "@/components/ImageCard";

export default {
  components: { Stack, StackItem, ImageCard },
  data() {
    return {
      images: [
        "https://images.unsplash.com/photo-1572111504021-40abd3479ddb?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80",
        "https://images.unsplash.com/photo-1542213167-80135ebd7f93?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8Y2l0cm9lbnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
		"https://images.unsplash.com/photo-1499549657095-91d25e1fd870?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8Y2l0cm9lbnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
		"https://images.unsplash.com/photo-1565992441121-4367c2967103?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTB8fHNwb3J0fGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
      ],
    };
  },
};
</script>

<template>
  <v-container>
    <div> Home Page </div>
    <stack :column-min-width="320" :gutter-width="8" :gutter-height="8">
      <stack-item v-for="(item, i) in images" :key="i">
        <image-card :url="item" />
      </stack-item>
    </stack>
  </v-container>
</template>

<style></style>
