<template>
  <div>
    <v-card>
      <v-card-title>
        Welcome to the Amazonless-Wish-List
      </v-card-title>
    </v-card>

    <RegistrationLogin />
  </div>
</template>

<script>
import RegistrationLogin from "../components/registerLogin/registerLogin";

export default {
  components: {
    RegistrationLogin
  }
};
</script>
