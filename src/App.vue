<template>
  <div>
      <app-header></app-header>
      <app-ChooseCard></app-ChooseCard>
      <app-Footer></app-Footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import ChooseCard from './components/ChooseCard.vue'
import Footer from './components/Footer.vue'
    
export default {
    components: {
        'app-header' : Header,
        'app-ChooseCard' : ChooseCard,
        'app-Footer' : Footer,
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
        font-family: 'Lato', sans-serif;
    }
</style>
