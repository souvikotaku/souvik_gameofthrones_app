<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Thronebox msg="Souvik Game of Thrones App"/>
</template>

<script>
import Thronebox from './components/Thronebox.vue'

export default {
  name: 'Game of thrones App',
  components: {
    Thronebox
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
