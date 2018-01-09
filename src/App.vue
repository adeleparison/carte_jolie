<template>
  <div>
      <app-header></app-header>
      <app-ChooseCard></app-ChooseCard>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import ChooseCard from './components/ChooseCard.vue'
    
export default {
    components: {
        'app-header' : Header,
        'app-ChooseCard' : ChooseCard,
    },
  data () {
    return {
    }
  }
}
</script>

<style>
    body {
        margin: 0;
    }
</style>
