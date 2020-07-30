<template>
  <div>
    <v-dialog v-model="dialog" width="500">
      <template v-slot:activator="{ on, attrs }">
        <v-btn v-bind="attrs" v-on="on"> Add Item</v-btn>
      </template>

      <v-card>
        <v-card-title>Add an Item </v-card-title>

        <v-card-text>
          <v-form ref="form">
            <v-flex>
              <v-text-field
                v-model="artist"
                label="Artist"
                outlined
                clearable
              ></v-text-field>
            </v-flex>
          </v-form>
        </v-card-text>

        <v-card-actions>
          <v-btn @click="clearForm">Cancel</v-btn>
          <v-spacer></v-spacer>
          <v-btn @click="addItem">Add</v-btn>
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
      dialog: false,
      artist: ""
    };
  },

  methods: {
    addItem() {
      console.log(this.artist);

      this.dialog = false;
    },

    clearForm() {
      this.$refs.form.reset();
      this.dialog = false;
    }
  }
};
</script>
