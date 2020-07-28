<template>
  <div id="app">
    <appQuote>
      <h2 slot="title">{{ quoteTitle }}</h2>
      <p slot="content">A wonderful quote</p>
    </appQuote>
  </div>
</template>

<script>
import Quote from './components/Quote.vue';

export default {
  data: function(){
      return {
        quoteTitle: 'The Quote'
      }
  },
  components: {
    appQuote: Quote
  }
}
</script>

<style scoped>
  
</style>
