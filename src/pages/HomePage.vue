<script>
import { Stack, StackItem } from "vue-stack-grid";
import ImageCard from "@/components/ImageCard";

export default {
  components: { Stack, StackItem, ImageCard },
  data() {
    return {
      images: [
        {
          url:
            "https://images.unsplash.com/photo-1519681393784-d120267933ba?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTN8fG1vdW50YWlufGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Selman Başkaya",
          job: "Computer Engineer",
          profileImg:
            "https://images.unsplash.com/photo-1610024062303-e355e94c7a8c?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjd8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1508923567004-3a6b8004f3d7?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTB8fG1vdW50YWlufGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Kübra Güveli",
          job: "Computer Engineer",
          profileImg:
            "https://images.unsplash.com/photo-1614567546037-d4347b1ff7ce?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8cHJvZmlsZSUyMGltYWdlfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1572111504021-40abd3479ddb?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80",
          name: "Ertan Çiller",
          job: "Computer Engineer Std.",
          profileImg:
            "https://images.unsplash.com/photo-1611774833580-40f2f588eaa4?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NHx8cHJvZmlsZSUyMGltYWdlfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1542213167-80135ebd7f93?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8Y2l0cm9lbnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Orhan Can İlişik",
          job: "Computer Engineer Std.",
          profileImg:
            "https://images.unsplash.com/photo-1610261003803-224ee66747e1?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Nnx8cHJvZmlsZSUyMGltYWdlfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1499549657095-91d25e1fd870?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8Y2l0cm9lbnxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Berat Doğru",
          job: "Software Developer",
          profileImg:
            "https://images.unsplash.com/photo-1577091379102-31fc6dc08626?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OXx8cHJvZmlsZSUyMGltYWdlfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1565992441121-4367c2967103?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTB8fHNwb3J0fGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Can Çağlayan",
          job: "Computer Engineer",
          profileImg:
            "https://images.unsplash.com/photo-1610478865542-7d239b415687?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTZ8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1559554498-7a9eb7587782?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NXx8dHVya2V5fGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Mustafa Arı",
          job: "Computer Engineer",
          profileImg:
            "https://images.unsplash.com/photo-1536057222397-e51989d3cb8a?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTd8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1529528553681-62a7d70dc888?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Nnx8dHVya2V5fGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Ferhat Keskin",
          job: "Computer Engineer Std.",
          profileImg:
            "https://images.unsplash.com/photo-1606513542745-97629752a13b?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MTh8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
        {
          url:
            "https://images.unsplash.com/photo-1518084823714-2f59a7315a39?ixid=MXwxMjA3fDB8MHxzZWFyY2h8M3x8aXN0YW5idWx8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
          name: "Mezun Var!",
          job: "Founder",
          profileImg:
            "https://images.unsplash.com/photo-1611774812120-79d97450b31c?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjR8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60",
        },
      ],
    };
  },
};
</script>

<template>
  <v-container>
    <stack :column-min-width="320" :gutter-width="10" :gutter-height="8">
      <stack-item v-for="(item, i) in images" :key="i">
        <image-card
          :url="item.url"
          :users="{ name: item.name, job: item.job, profileImg: item.profileImg }"
        />
      </stack-item>
    </stack>
  </v-container>
</template>

<style></style>
