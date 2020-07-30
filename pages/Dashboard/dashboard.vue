<template>
  <div>
    <h1>this is the dashboard.</h1>

    <ListFilter />

    <AddItemDialog />

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
import ListFilter from "../../components/filters/listFilter";
import AddItemDialog from "../../components/dialogs/addItem/addItemDialog";

export default {
  name: "Dashboard",

  components: {
    ItemDisplay,
    ListFilter,
    AddItemDialog
  },

  data() {
    return {};
  }
};
</script>
