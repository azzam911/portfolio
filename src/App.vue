<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <router-link  to="/" class="navbar-brand" >Azzam Alkhaldi</router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
      </ul>
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item items">
          <router-link to="/">Home</router-link> |
          <router-link to="/about">About</router-link> |
          <router-link to="/projects">projects</router-link>
        </li>
        </ul>
        
    </div>
  </div>
</nav>
  <router-view/>
</template>
<script>
  export default {
    name: "App",
    
  }
</script>
<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  text-align: center;
  text-decoration: none !important;
}
nav {
    display: flex;
    padding: 30px;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 0 12px #eee;
    margin-bottom: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
}
a:hover {
  color: #42b983 !important;
}
nav a.router-link-exact-active {
  color: #42b983;
}
.name {
  font-size: 20px;
  font-weight: bold;
}
.mob-list .main-spn {
    display: inline-block;
    position: relative;
    width: 30px;
    cursor: pointer;
}
.mob-list .main-spn span {
    width: 100%;
    height: 3px;
    display: block;
    background-color: #000;
    margin: 5px;
}
.navbar-nav {
  text-align: right !important;
  margin: 20px 0 !important;

}
.navbar-collapse {
  transition: .5s !important;
}

@media screen and (min-width: 992px) {
    .items {
    margin-left: 500px;
  }
}
@media screen and (min-width: 1066px) {
    .items {
    margin-left: 700px;
  }
}


</style>
