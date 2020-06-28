<template>
  <div id="app">

    <Header/>
    <Categories/>

    <router-link to="/">List</router-link>
    <router-link to="/detail">Detail</router-link>

     <router-view></router-view>
  </div>
</template>

<script>
import Header  from './components/Header'
import Categories  from './components/Categories'

export default {
  name: 'App',
  components: {
    Header,
    Categories
  }
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
