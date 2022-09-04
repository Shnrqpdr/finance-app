<template>
  <v-container>
    <v-app-bar app flat>
      <v-button>
        <v-icon
          large
          class="dark-mode"
          @click="$vuetify.theme.dark = !$vuetify.theme.dark"
          >mdi-theme-light-dark</v-icon
        >
      </v-button>
      <v-spacer />
      <v-button>
        <v-icon large @click="sair()">mdi-exit-to-app</v-icon>
      </v-button>
    </v-app-bar>
    <v-row class="text-center">
      <v-col cols="3"> <v-sheet height="50vh" rounded="lg"></v-sheet> </v-col>
      <v-col cols="9" class="mb-4">
        <v-sheet height="50vh" rounded="lg"></v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HomePage",

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
