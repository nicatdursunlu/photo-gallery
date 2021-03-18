<template>
  <v-container fluid>
    <v-app-bar color="deep-purple accent-4" dark>
      <v-spacer />
      <v-btn oulined class="ml-3">
        <router-link to="/">Home</router-link>
      </v-btn>
      <v-btn oulined class="ml-3">
        <router-link to="/photo">Photos</router-link>
      </v-btn>
    </v-app-bar>
  </v-container>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>