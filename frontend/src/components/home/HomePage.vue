<template>
  <v-container>
    <v-app-bar app flat>
      <v-btn depressed>
        <v-icon
          large
          class="dark-mode"
          @click="$vuetify.theme.dark = !$vuetify.theme.dark"
          >mdi-theme-light-dark</v-icon
        >
      </v-btn>
      <v-spacer />
      <v-btn depressed>
        <v-icon large @click="sair()">mdi-exit-to-app</v-icon>
      </v-btn>
    </v-app-bar>

    <v-row class="text-center">
      <v-col cols="2" xl="2" xs="4">
        <v-navigation-drawer height="50vh" permanent expand-on-hover>
          <profile />
        </v-navigation-drawer>
      </v-col>
      <v-col cols="10" xl="10" xs="8" class="mb-4">
        <v-sheet rounded="lg">
          <principal-finances />
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Profile from "./Profile";
import PrincipalFinances from "./PrincipalFinances";

export default {
  name: "HomePage",
  components: {
    Profile,
    PrincipalFinances,
  },

  data: () => ({}),
  methods: {
    sair() {
      this.$router.push("/");
    },
  },
};
</script>
<style lang="scss" scoped>
.dark-mode {
  cursor: pointer;
}
</style>
