<template>
  <v-app id="inspire">
    <v-main class="background">
      <v-container style="height: 100%">
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
};
</script>
<style lang="scss" scoped>
.background {
  background-color: #0a0e5098;
}

.container {
  height: 100%;
}
</style>
