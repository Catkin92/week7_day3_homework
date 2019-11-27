<template>
  <div v-if='country' class="country-detail" :style="{ backgroundImage: `url(${country.flag})` }">
    <h3>{{ country.name }}</h3>
    <p>Capital: {{ country.capital }}</p>
    <p>Population: {{ country.population }}</p>
    <h3>Languages:</h3>
    <ul>
      <li v-for="language in country.languages">{{language.name}}</li>
    </ul>
  </div>
</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: 'country-detail',
  props: ['country'],

}
</script>

<style lang="css" scoped>
  .country-detail {
    height: 300px;
    width: 500px;
    background-size: cover;
    color: white;
    padding: 10px;
    font-size: 20px;
    font-family: monospace;
    text-shadow: 2px 1px black;
  }
</style>
