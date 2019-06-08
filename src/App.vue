<template>
  <div id="app">
    <Navbar />
    <router-view id="content" />
  </div>
</template>

<script>
import Navbar from './components/Navbar'

export default {
  name: 'app',
  components: { Navbar
  }
}
</script>

<style>

body {
  margin: 0px;
  padding: 0px;
}   

#content {
  width: 70%;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: left;
  color: #2c3e50;
}

</style>
