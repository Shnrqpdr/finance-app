<template>
  <v-container>
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
    <v-row class="row-card-login">
      <v-col cols="12" sm="6">
        <v-sheet height="50vh" rounded="lg">
          <login-page />
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import LoginPage from "../components/login/LoginPage";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Login",
  data: () => ({
    links: ["Login", "About", "Github"],
  }),
  components: {
    LoginPage,
  },
};
</script>
<style scoped>
.row-card-login {
  justify-content: center;
  align-items: center;
  height: 100%;
}
</style>
