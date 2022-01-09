<template>
  <div class="home">
    <div class="home-content">
      <div class="head">
        <h1 class="welcome">
          WELCOME TO<span class="the"><h4>THE</h4></span>
        </h1>
        <span class="nawky"><h1>NAWKY</h1></span>
      </div>
      <div class="sub">
        <p>
          NAWKY Club is a group of people who want to improve themselves in
          various fileds. Let's share experiences and opinions!
        </p>
      </div>
      <div class="button">
        <button class="discord" @click="inviteLink">
          <img src="../assets/discord-seeklogo.com.svg" alt="" />
        </button>
        <router-link to="/leaderboard" class="link">
          <button class="leaderboard"><p>LEADERBOARD</p></button>
        </router-link>
      </div>
    </div>
    <div class="home-image">
      <img src="../assets/content_1.png" alt="" />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  methods: {
    inviteLink () {
      window.open('https://discord.gg/nEhfgdY2U6', '_blank')
    }
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Libre+Franklin:wght@800&display=swap");
.home {
  background-color: #19003c;
  display: flex;
  width: 100%;
  height: 82.1vh;
  align-items: center;
  justify-content: space-evenly;
}

.home-content {
  display: flex;
  flex-direction: column;
  flex-basis: 600px;
}

.head {
  position: inline-box;
}

.welcome,
.the,
.nawky {
  font-family: "Glacial-Indifference-Regular";
}

.welcome {
  font-family: "Libre Franklin", sans-serif;
  font-weight: bold;
  color: #fff;
  font-size: 40pt;
}

.the > h4 {
  font-family: "Libre Franklin", sans-serif;
  margin: -5px 270px 0px 0px;
  font-size: 20pt;
}

.nawky > h1 {
  font-family: "Libre Franklin", sans-serif;
  font-weight: bold;
  font-size: 46pt;
  color: #19003c;
  -webkit-text-stroke: 1px white;
  letter-spacing: 5px;
  margin-left: 70px;
  margin-top: -75px;
}

.sub {
  width: 400px;
  text-align: left;
  margin-top: 2rem;
  margin-left: 140px;
}

.sub > p {
  font-size: 16pt;
}

.home-image > img {
  width: 911px;
}

.button {
  display: flex;
  justify-content: space-evenly;
  padding: 0 4rem;
}

.discord,
.leaderboard {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 150px;
  height: 40px;
  border-radius: 1rem;
}

.discord {
  background-color: transparent;
  border: 2px solid white;
  color: white;
  font-family: "Libre Franklin", sans-serif;
  cursor: pointer;
}

.discord > img {
  height: 50px;
}

.leaderboard {
  background-color: white;
  color: #19003c;
  font-family: "Libre Franklin", sans-serif;
  font-weight: bold;
  cursor: pointer;
}

.leaderboard > p {
  font-size: 11pt;
}

.link{
  text-decoration: none;
}
</style>