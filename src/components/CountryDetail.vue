<template lang="html">

<main v-if="country">
  <h3>{{country.name}}</h3>
  <p>{{country.capital}}</p>
  <p>{{country.population}}</p>
  <p v-for="(language, index) in country.languages">Languages: {{language.name}}</p>
  <img :src="country.flag" height="200" width="300"/>
</main>

</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
