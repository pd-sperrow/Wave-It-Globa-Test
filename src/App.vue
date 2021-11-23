<template>
  <div id="app">
    <section class="content mt-4">
      <search-manager />
      <search-details />
    </section>
  </div>
</template>

<script>
import SearchManager from './components/SearchManager/SearchManager.vue'
import SearchDetails from './components/SearchDetails/SearchDetails.vue'

export default {
  name: 'App',
  components: {
    SearchManager,
    SearchDetails
  },
  data () {
    return {
      title: 'Wave it global'
    }
  }
}
</script>

<style>
  @import './assets/css/main.css';
</style>
<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
  }
  .content {
    position: relative;
    width: 100%;
    display: flex;
  }
</style>
