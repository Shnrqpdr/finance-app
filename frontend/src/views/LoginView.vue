<template>
  <v-row class="row-card-login">
    <v-col cols="12" sm="6">
      <v-sheet height="50vh" rounded="lg">
        <login-page />
      </v-sheet>
    </v-col>
  </v-row>
</template>

<script>
import LoginPage from "../components/login/LoginPage";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Login",

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
