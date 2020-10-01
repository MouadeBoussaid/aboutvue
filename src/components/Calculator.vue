<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col cols="12" sm="3">
          <v-text-field
            v-model="inputField1"
            type="number"
            outlined
          ></v-text-field>
        </v-col>

        <v-col cols="12" sm="2">
          <v-select
            v-model="operator"
            :items="operators"
            outlined
            type="text"
          ></v-select>
        </v-col>
        <v-col cols="12" sm="3">
          <v-text-field
            v-model="inputField2"
            type="number"
            outlined
          ></v-text-field>
        </v-col>

        <v-col cols="12" sm="2">
          <v-text-field v-model="outputCalc" disabled></v-text-field>
        </v-col>
        <v-col cols="12" sm="2">
          <v-btn
            @click="saveCalc()"
            class="mx-2"
            elevation="5"
            fab
            dark
            color="primary"
          >
            <v-icon dark>
              mdi-plus
            </v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-col cols="12" sm="10">
        <v-card class="mx-auto" max-width="500" min-height="300" tile>
          <v-list dense>
            <v-list-item v-for="(item, i) in calcData" :key="i">
              <v-list-item-content>
                <v-list-item-title> {{ item }}</v-list-item-title>
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
      inputField1: 0,
      inputField2: 0,
      calcData: [],
      operators: ["x", "-", "+", "/"],
      operator: "x"
    };
  },
  methods: {
    saveCalc() {
      this.calcData.push(this.calculate(this.inputField1, this.inputField2));
    },
    calculate(x, y) {
      let operatorFn;
      switch (this.operator) {
        case "+":
          operatorFn = (x, y) => parseInt(x) + parseInt(y);
          break;
        case "x":
          operatorFn = (x, y) => parseInt(x) * parseInt(y);
          break;
        case "-":
          operatorFn = (x, y) => parseInt(x) - parseInt(y);
          break;
        case "/":
          operatorFn = (x, y) => parseInt(x) / parseInt(y);
          break;
      }
      return operatorFn(x, y);
    }
  },
  computed: {
    outputCalc() {
      return this.calculate(this.inputField1, this.inputField2);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
