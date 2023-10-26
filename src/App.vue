<template>
  <ul>
    <learning-resources
      v-for="resource in storedResources"
      :key="resource.id"
      :resource="resource"
    ></learning-resources>
  </ul>
</template>

<script>
import LearningResources from "./components/learning-resources/LearningResources.vue";

export default {
  components: {
    LearningResources,
  },

  data() {
    return {
      storedResources: [
        {
          id: "official-guide",
          title: "Official Guide",
          description: "The official Vue.js documentation",
          link: "https://vuejs.org/",
        },
        {
          id: "google",
          title: "Google",
          description: "Learn to google",
          link: "https://google.com/",
        },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap");

* {
  box-sizing: border-box;
}

html {
  font-family: "Roboto", sans-serif;
}

body {
  margin: 0;
}
</style>
