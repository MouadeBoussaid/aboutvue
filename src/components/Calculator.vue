<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col cols="12" sm="3">
          <v-text-field type="number" outlined></v-text-field>
        </v-col>

        <v-col cols="12" sm="2">
          <v-select :items="operators" outlined type="text"></v-select>
        </v-col>
        <v-col cols="12" sm="3">
          <v-text-field type="number" outlined></v-text-field>
        </v-col>

        <v-col cols="12" sm="2">
          <v-text-field disabled></v-text-field>
        </v-col>
        <v-col cols="12" sm="2">
          <v-btn class="mx-2" elevation="5" fab dark color="primary">
            <v-icon dark>
              mdi-plus
            </v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-col cols="12" sm="10">
        <v-card class="mx-auto" max-width="500" min-height="300" tile>
          <v-list dense>
            <v-list-item>
              <v-list-item-content>
                <v-list-item-title></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-container>
  </v-form>
</template>

<script>
export default {
  name: "Calculator",
  data() {
    return {
      operators: ["x", "-", "+", "/"]
    };
  },
  methods: {},
  computed: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
