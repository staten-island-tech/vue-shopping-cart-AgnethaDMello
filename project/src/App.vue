<template>
  <div id="app">
    <h1 id="header">Framblees!</h1>
    <div id="frankie">
      <h2>These are all made by my friend Frankie! Visit his shop!</h2>
      <a href="https://www.etsy.com/shop/FrambleesArt">Etsy Shop</a>
    </div>
    <router-view />
  </div>
</template>

<style>
body {
  background-color: rgb(197, 235, 235);
}

#app {
  font-family: Comic Sans MS, Comic Sans, cursive;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

h1 {
  text-align: center;
  font-size: 5rem;
  color: rgb(20, 69, 150);
  padding: 3rem;
  background-color: darkseagreen;
  margin-top: 0rem;
  border: solid 1rem rgb(61, 102, 97);
}

#frankie {
  color: rgb(17, 17, 109);
  margin-bottom: 1rem;
  font-size: 1rem;
}

#nav {
  padding: 0rem;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
