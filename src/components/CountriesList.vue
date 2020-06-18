<template lang="html">
  <div>
    <select @change=onChange() v-model="selectedCountry">
      <option v-for="(country, index) in countries" :value="country" :key="index">{{country.name}}</option>
    </select>
  </div>

</template>

<script>
import { eventBus } from '../main.js';


export default {
  name: 'countries-list',
  props: ['countries','country'],



  methods: {
  handleSelect(){
      eventBus.$emit('country-selected', this.value)

  },
  onChange(){
      eventBus.$emit('country-selected', this.selectedCountry)

  }

  }


}
</script>
