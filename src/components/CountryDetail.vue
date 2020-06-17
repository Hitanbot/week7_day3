<template lang="html">

  <div>
  <div v-if='country'>
    <h3>{{country.name}}</h3>
    <p>Capital: {{country.capital}}</p>
    <p>Region: {{country.region}}</p>
    <p>Population: {{country.population}}</p>
    </div>
  </div>
</template>

<script>


export default {
  name: 'country-detail',
  props: ['country']
}

</script>

<style lang="css" scoped>
</style>
