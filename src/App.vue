<template>
  <div class="App">
    
      <input 
      placeholder="Enter your name" 
      v-model="name">
      

      <div class="greeting">Hello {{ name }}!</div>

      <search-result v-if="showSearchResult" v-bind:name-attribute="name"></search-result>
  </div>
</template>

<script>
  
  export default {

    data() {
      return {
        name: '',
        showSearchResult: window.showSearchResult
      } 
    } 

  }
</script>    

<style>
.App {
  margin-top: 30px;
  text-align: center;
}
.greeting {
  margin-top: 20px;
}
</style>