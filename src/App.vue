<template>
  <search-bar
  @sent="submit"
  ></search-bar>
  
</template>

<script>
import SearchBar from './components/SearchBar.vue'
export default {
  name: 'App',
  components: {
    SearchBar
  },
  
  data() {
    return  {
      accessKey: 'qn72mmKiEZ6vI4hvj4aeHsXcyrPzqhkmAg9P_UtyV04',
      url: 'https://api.unsplash.com/photos/random',
      photos: '',
      keyword: 'erer'
    }
  },
  methods: {
    submit(val) {
      this.keyword = val;
    }
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
