<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col cols="12" md="4">
          <v-autocomplete
            v-model="name"
            :items="allnames"
            :loading="loading"
            :search-input.sync="search"
            color="white"
            hide-no-data
            hide-selected
            item-text="Description"
            item-value="API"
            label="Name"
            placeholder="Start typing to Search"
            prepend-icon="mdi-cards-outline"
            return-object
          ></v-autocomplete>
        </v-col>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="rules"
            label="Rules text"
            append-icon="mdi-plus-circle"
            @click:append="showSymbols"
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="4">
          <v-autocomplete
            v-model="types"
            :items="allnames"
            chips
            small-chips
            label="Type"
            multiple
          ></v-autocomplete>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>
<script>
export default {
  name: "cardFilter",
  data: () => ({
    name: "",
    valid: null,
    loading: false,
    search: "",
    allnames: [],
    types: [],
    allTypes: []
  }),
  methods: {
    showSymbols() {
      alert();
    }
  }
};
</script>
