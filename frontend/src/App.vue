<template>
  <v-app id="inspire">
    <v-app-bar app flat>
      <v-avatar
        :color="$vuetify.breakpoint.smAndDown ? 'grey darken-1' : 'transparent'"
        size="32"
      ></v-avatar>

      <v-tabs centered class="ml-n9" color="grey darken-1">
        <v-tab v-for="link in links" :key="link">
          {{ link }}
        </v-tab>
      </v-tabs>

      <v-icon
        large
        class="dark-mode"
        @click="$vuetify.theme.dark = !$vuetify.theme.dark"
        >mdi-theme-light-dark</v-icon
      >
    </v-app-bar>

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

  data: () => ({
    links: ["Login", "About", "Github"],
  }),
};
</script>
<style lang="scss" scoped>
.background {
  background-color: #0a0e5098;
}

.dark-mode {
  cursor: pointer;
}
</style>
