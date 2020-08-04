<template>
  <div id="app">
    <button @click="selectedComponent = 'appQuote'">Quote</button>
    <button @click="selectedComponent = 'appAuthor'">Author</button>
    <button @click="selectedComponent = 'appNew'">New</button>
    <hr>
    <keep-alive>
      <component :is="selectedComponent">
        Deafult Content
      </component>
    </keep-alive>
    
    <!-- <appQuote>
      <h2 slot="title">{{ quoteTitle }}</h2>
      <p slot="content">A wonderful quote</p>
    </appQuote> -->
  </div>
</template>

<script>
import Quote from './components/Quote.vue';
import Author from './components/Author.vue';
import New from './components/New.vue';
export default {
  data: function(){
      return {
        quoteTitle: 'The Quote',
        selectedComponent: 'appQuote'
      }
  },
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
  }
}
</script>

<style scoped>
  
</style>
