<template>
  <v-container>
    <Photo v-for="(photo, index) in photos" :key="index" />
  </v-container>
</template>

<script>
import Photo from "../components/photo/Photo";

export default {
  components: {
    Photo,
  },
  data: () => ({
    photos: [
      { id: 1, title: "Photo 1" },
      { id: 2, title: "Photo 2" },
      { id: 3, title: "Photo 3" },
      { id: 4, title: "Photo 4" },
    ],
  }),
};
</script>

<style lang="scss" scoped>
</style>