<template>
  <div>
    <nav>
      <router-link id='link' to='/' exact>Home</router-link>
      <router-link id='link' to='/about' exact>About</router-link>
      <a id='link' target="_blank" href="https://github.com/eltsu7/">GitHub</a>
      <a id='link' target="_blank" href="https://eeli.kuvat.fi/">Gallery</a>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'navbar'
}
</script>

<style scoped>
nav {
  margin: 0px;
  padding: 0px;
  overflow: hidden;
  list-style-type: none;
  display: block;
  background-color: #333;
}

#link {
  float: left;
  display: block;
  color: white;
  text-align: center;
  padding: 16px 20px;
  text-decoration: none;
}

#link.router-link-active {
  color: #bbb;
  background-color: #444;
}

#link:hover {
  background-color: #555;
}


</style>
