<template>
  <v-dialog
    v-model="$store.getters.getDialogVisible"
    @click:outside="$store.commit('hideDialog')"
    max-width="600"
  >
    <v-card>
      <v-card-title>{{ fullTitle }}</v-card-title>
      <v-card-text>
        <v-img :src="$store.getters.getCurrentPhoto.url" />
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  computed: {
    fullTitle() {
      return `Title of the photo is ${this.$store.getters.getCurrentPhoto.title}`;
    },
  },
};
</script>

<style lang="scss" scoped>
</style>