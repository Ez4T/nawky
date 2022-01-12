<template>
  <div id="nav">
    <div class="logo">
      <div class="logo-img">
        <img src="./assets/nawky.png" alt="nawky" />
      </div>
      <div class="logo-content">
        <span class="main"><h1>NAWKY</h1></span>
        <span class="sub"><p>NOT ACTIVE WE KICK YOU</p></span>
      </div>
    </div>
    <div class="menu">
      <div class="menu-content">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/leaderboard">Leaderboard</router-link>
      </div>
    </div>
  </div>
  <router-view />
</template>

<style>
@font-face {
  font-family: "Glacial-Indifference-Regular";
  src: url("./fonts/glacial/Glacial-Indifference-Regular.ttf.woff")
      format("woff"),
    url("./fonts/glacial/Glacial-Indifference-Regular.ttf.svg#Glacial-Indifference-Regular")
      format("svg"),
    url("./fonts/glacial/Glacial-Indifference-Regular.ttf.eot"),
    url("./fonts/glacial/Glacial-Indifference-Regular.ttf.eot?#iefix")
      format("embedded-opentype");
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: "zing-rust-base";
  src: url("./fonts/zing_rust/ZingRustG1-Trial-Base.woff") format("woff"),
    url("./fonts/zing_rust/ZingRustG1-Trial-Base.woff2") format("woff2"),
    url("./fonts/zing_rust/ZingRustG1-Trial-Base.eot"),
    url("./fonts/zing_rust/ZingRustG1-Trial-Base.eot?#iefix")
      format("embedded-opentype");
  font-weight: normal;
  font-style: italic;
}

h1 {
  font-family: "Glacial-Indifference-Regular";
}

body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: "Glacial-Indifference-Regular";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #19003c;
}

#nav a {
  font-family: "Glacial-Indifference-Regular";
  font-weight: bold;
  color: #fff;
  margin-right: 132px;
  text-transform: uppercase;
  text-decoration: none;
  font-size: 14pt;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.logo {
  margin: 0 8.5rem;
  padding: 0 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Start left-navbar */

.logo-img > img {
  width: 170px;
}

.logo-content {
  margin-bottom: 20px;
}

.main > h1 {
  margin-left: -55px;
  font-family: "zing-rust-base";
  color: white;
  letter-spacing: 4px;
  font-size: 36pt;
}

.sub > p {
  font-family: "Glacial-Indifference-Regular";
  color: white;
  font-size: 13pt;
  margin-top: -40px;
  margin-left: -25px;
}

/* End loft-navbar */
/* Start right-navbar */
.menu {
  margin: 0 1.5rem;
  padding: 1rem 1rem;
}
</style>
