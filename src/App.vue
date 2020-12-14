<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>
    <a href="assets/csv-sample.csv">Sample CSV</a>
  </div>
  <div>
    <vue-csv-import v-model="mappedCsv" :fields="fields">
      <div>
        <vue-csv-toggle-headers></vue-csv-toggle-headers>
      </div>
      <div>
        <vue-csv-errors></vue-csv-errors>
      </div>
      <div>
        <vue-csv-input></vue-csv-input>
      </div>
      <div>
        <vue-csv-map></vue-csv-map>
      </div>
    </vue-csv-import>
  </div>
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
export default {
  name: "App",
  data() {
    return {
      mappedCsv: [],
      fields: {
        name: { required: false, label: "Name" },
        age: { required: true, label: "Age" },
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
