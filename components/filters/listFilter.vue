<template>
  <div>
    <v-text-field
      v-model="filterTerm"
      label="Filter List..."
      outlined
      clearable
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
  }
};
</script>
