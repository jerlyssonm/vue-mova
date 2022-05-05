<template>
  <div>
    <HeaderPage/>
    <HomePage />
    <FooterPage />
  </div>
</template>

<script>
import HeaderPage from './components/HeaderPage.vue'
import HomePage from './components/HomePage.vue'
import FooterPage from './components/FooterPage.vue'

export default {
  name: '',
  components: {
    HeaderPage,
    HomePage,
    FooterPage,
  },
}
</script>

<style>
*{  
  padding: 0;
  margin: 0;
  border: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
