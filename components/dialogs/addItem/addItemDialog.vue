<template>
  <div>
    <v-dialog v-model="dialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on"> Add Item</v-btn>
      </template>

      <v-card>
        <v-card-title>Add an Item </v-card-title>

        <v-card-text>
          <v-flex>
            <v-text-field label="Artist" outlined clearable></v-text-field>
          </v-flex>
        </v-card-text>

        <v-card-actions>
          <v-btn>Cancel</v-btn>
          <v-spacer></v-spacer>
          <v-btn>Add</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  name: "AddItemDialog",

  data() {
    return {
      dialog: false
    };
  }
};
</script>
