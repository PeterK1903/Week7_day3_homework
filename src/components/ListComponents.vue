<template lang="html">
  <div class="">
    <li v-on:click="handleClick">{{country.name}}</li>
    </select>


  </div>
</template>

<script>
import {eventBus} from '../main.js'

export default {
  name: 'list-component',
  props: ['country'],
  methods: {
    handleClick(){
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style lang="css" scoped>
</style>



<label for="from_rate_select">Select a Rate:</label>
      <select id="from_rate_select" v-model.number="selectedRate">
        <option disabled value="">Select a Rate</option>
        <option v-for="(value, key) in ratesData.rates" v-bind:value="value"> {{key}} </option>
      </select>
