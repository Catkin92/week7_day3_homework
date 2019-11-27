<template>
  <div v-if='country'>
    <h3>{{ country.name }}</h3>
  </div>
</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
