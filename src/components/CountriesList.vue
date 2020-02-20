<template lang="html">

<main>
  <form>
 <label for="select-country">Select a country:</label>
 <select id="select-country" v-on:change="handleChange" v-model="country">
   <option disabled value="">Select a country</option>
   <option v-for="(country, index) in countries" :value="country" :key="index">{{country.name}}</option>
 </select>
</form>
</main>

</template>

<script>

import {eventBus} from '../main.js'

export default {
  name: 'countries-list',
  data(){
    return{
    country: null
    }
  },
  props: ['countries'],
  methods: {
    handleChange(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
