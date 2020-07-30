<template>
  <v-app dark>
    <v-app-bar fixed app>
      <router-link to="/Dashboard/dashboard">
        <v-toolbar-title v-text="title" />
      </router-link>

      <v-spacer />
      <router-link to="/">logout</router-link>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>

    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }} Holger Mueller</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      title: "Amazonless-Wish-List"
    };
  }
};
</script>
