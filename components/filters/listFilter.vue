<template>
  <div>
    <v-text-field
      v-model="filterTerm"
      label="Filter List..."
      outlined
      clearable
      :rules="[filterThroughList]"
    ></v-text-field>
  </div>
</template>

<script>
export default {
  name: "ListFilter",

  data() {
    return {
      filterTerm: ""
    };
  },

  computed: {
    filterThroughList() {
      console.log(this.filterTerm);
    }
  }
};
</script>
