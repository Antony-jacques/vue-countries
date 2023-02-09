<template>
  <div>
    <h1>Countries List</h1>
    <ul>
      <li v-for="(country, index) in countriesCollection" :key="index" >
        <CountryItem />
      </li>
    </ul>
  </div>
</template>
<script>
import CountryItem from "@/components/CountryItem";

export default {
  name: "countriesListView",
  components: { CountryItem },
  data() {
    return {
      countriesCollection: null,
      test: "toto"
    };
  },
  mounted() {
    try {
      fetch("https://restcountries.com/v3.1/all")
        .then(response => response.json())
        .then(response => {
          this.countriesCollection = response;
          console.log(this.countriesCollection);
        });
      console.log(this.countriesCollection);
    } catch (error) {
      console.log(error);
    }
  }
};
</script>