<template>
  <div id="login">
    <v-form ref="form">
      <v-flex xs12 sm12 md12 lg12 xl12>
        <v-text-field label="Email" outlined></v-text-field>
      </v-flex>

      <v-flex xs12 sm12 md12 lg12 xl12>
        <v-text-field label="Password" outlined></v-text-field>
      </v-flex>
    </v-form>

    <v-divider></v-divider>

    <v-card-actions>
      <v-btn>Cancel</v-btn>
      <v-spacer></v-spacer>
      <v-btn>Log in</v-btn>
    </v-card-actions>
  </div>
</template>

<script>
export default {
  name: "Login",

  data() {
    return {};
  }
};
</script>
