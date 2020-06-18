<template lang="html">
  <option :value="country" @change="onChange()">{{country.name}}</option>
</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: 'list-item',
  props: ['country'],
  methods: {
  onChange(){
      eventBus.$emit('country-selected', this.country)

  }

  }
}
</script>

<style lang="css" scoped>
</style>
