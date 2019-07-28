<template>
  <div>
    <nav>
      <li>
        <router-link id='link' to='/' exact>About</router-link>
      </li>
      <li>
        <a id='link' href="http://eelih.fi/blog/">Blog</a>
      </li>
      <li>
        <a id='link' target="_blank" href="https://github.com/eltsu7/">GitHub</a>
      </li>
      <li>
        <a id='link' target="_blank" href="https://eeli.kuvat.fi/">Gallery</a>
      </li>
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
  margin: 0 auto;
  padding: 0px;
  overflow: hidden;
  list-style: none;
  background-color: #333;
  text-align: center;
}

nav li {
  display: inline;
}

#link {
  display: inline-block;
  color: white;
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
