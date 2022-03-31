<template>
  <div>
    <h2>Creating APIs</h2>
    <div>
      <b-form-input v-model="text" placeholder="Enter train name">
      </b-form-input>
    </div>
    <br />

    <b-button @click="getData()">Search Data</b-button>

    <div>
      {{ searchData.data }}
    </div>
    <br /><br /><br />
    <table align="center">
      <thead>
        <tr>
          <th>continent</th>
          <th>Region</th>
          <th>Country</th>
          <th>Capital</th>
          <th>fips</th>
          <th>iso2</th>
          <th>iso3</th>
          <th>isoNo</th>
          <th>internet</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="user in searchData.data" :key="user.id">
          <td>{{ user.continent }}</td>
          <td>{{ user.region}}</td>
          <td>{{ user.country }}</td>
          <td>{{ user.capital }}</td>
          <td>{{ user.fips }}</td>
          <td>{{user.iso2}}</td>
        <td>{{user.iso3}}</td>
        <td>{{user.isoNo}}</td>
        <td>{{user.internet}}</td>


        </tr>
      </tbody>
    </table>
  </div>
</template>
<script>
var axios = require("axios").default;

export default {
  name: "sampleApis",

  data() {
    return {
     
      
      options: {
        method: "POST",

        url: "https://github.com/richorama/country-code-lookup/blob/master/index.js/",

       // headers: {
          //"content-type": "application/json",

          //"X-RapidAPI-Host": "trains.p.rapidapi.com",

          //"X-RapidAPI-Key":"0030c715ecmsh58180c0530cc6e6p188880jsncda365dc0d9f",
        //},

        data: { search: "" },
      },

      text: "",

      searchData: {},
    };
  },

  methods: {
    async getData() {
      this.options.data.search = this.text;
      this.searchData = await axios.request(this.options);
    },
  },
};
</script>

<style scoped>
table {
  font-family: arial;

  border-collapse: collapse;

  width: 60%;

  text-align: center;
}

td,
th {
  border: 3px solid #dddddd;

  text-align: center;

  padding: 8px;
}
</style>