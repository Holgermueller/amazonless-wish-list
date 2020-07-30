<template>
  <div>
    <h1>this is the dashboard.</h1>

    <div>
      <v-card>
        <v-card-title></v-card-title>
        <v-card-text>
          <ItemDisplay />
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
import ItemDisplay from "./itemDisplay";

export default {
  name: "Dashboard",

  components: {
    ItemDisplay
  },

  data() {
    return {};
  }
};
</script>
