<template>
  <v-container class="fields-login">
    <v-row class="row-login">
      <v-col cols="12" sm="10">
        <v-text-field
          v-model="email"
          :rules="[rules.required, rules.email]"
          label="E-mail"
        ></v-text-field>
        <v-text-field v-model="password" label="Senha"></v-text-field>
      </v-col>
      <v-col cols="12" sm="10">
        <v-flex class="botoes">
          <div>Esqueci minha senha</div>
          <v-btn class="ma-2" color="#0a0e5098" @click="login()">
            Entrar <v-icon right> mdi-arrow-right </v-icon>
          </v-btn>
        </v-flex>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "LoginPage",

  data: () => ({
    email: "",
    password: "",
    rules: {
      required: (value) => !!value || "E-mail inválido.",
      counter: (value) => value.length <= 20 || "Max 20 characters",
      email: (value) => {
        const pattern =
          /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
        return pattern.test(value) || "Invalid e-mail.";
      },
    },
  }),
  methods: {
    login() {
      this.$router.push("/home");
    },
  },
};
</script>
<style lang="scss" scoped>
.fields-login {
  width: 100%;
  height: 100%;
}

.row-login {
  height: 100%;
  justify-content: center;
  align-items: center;
}

.botoes {
  display: flex;
  justify-content: space-between;
  align-items: center;

  div {
    font-size: 14px;
    text-decoration: underline;
    cursor: pointer;
  }
}
</style>
