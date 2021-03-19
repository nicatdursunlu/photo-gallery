<template>
  <v-container>
    <PhotoForm @addPhoto="addPhoto" />
    <v-row>
      <Photo
        v-for="(photo, index) in $store.getters.getAllPhotos"
        :key="index"
        :photo="photo"
      />
    </v-row>
    <PhotoDialog />
  </v-container>
</template>

<script>
import { mapActions } from "vuex";
import Photo from "../components/photo/Photo";
import PhotoForm from "../components/photo/PhotoForm";
import PhotoDialog from "../components/photo/PhotoDialog";

export default {
  components: {
    Photo,
    PhotoForm,
    PhotoDialog,
  },
  data: () => ({
    photos: [],
  }),
  mounted() {
    this.fetchPhotos();
  },
  methods: {
    ...mapActions(["fetchPhotos"]),
    addPhoto(photo) {
      this.photos.unshift(photo);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>