<template>
  <div id="registerLogin">
    <v-card class="register-login" width="500">
      <v-tabs v-model="tab" fixed-tabs>
        <v-tab v-for="(form, index) in forms" :key="index">
          <h2>
            <span :class="form.icon"></span>
            {{ form.formName }}
          </h2>
        </v-tab>
      </v-tabs>

      <v-tabs-items v-model="tab">
        <v-tab-item v-for="(form, index) in forms" :key="index">
          <v-card>
            <v-card-title class="text-center">
              <h3>{{ form.message }}</h3>
            </v-card-title>

            <v-card-text>
              <div v-if="form.formName === 'Register'">
                <RegistrationForm />
              </div>

              <div v-else>
                <LoginForm />
              </div>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </div>
</template>

<script>
import RegistrationForm from "./register";
import LoginForm from "./login";

export default {
  name: "RegistrationLogin",

  components: {
    RegistrationForm,
    LoginForm
  },

  data() {
    return {
      tab: null,
      forms: [
        {
          formName: "Register",
          message: "Register Here:",
          icon: "mdi mdi-pen"
        },

        {
          formName: "Log in",
          message: "Log In Here:",
          icon: "mdi mdi-keyboard"
        }
      ]
    };
  }
};
</script>

<style scoped>
.register-login {
  margin: 9% auto;
}
</style>
