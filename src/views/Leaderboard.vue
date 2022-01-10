<template>
  <div class="about">
    <h1>This is a Leaderboard page</h1>
    <!-- <p>{{ users }}</p> -->
    <table class="table-auto">
      <thead>
        <tr>
          <td>Rank</td>
          <td>Name</td>
          <td>Point</td>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in users" :key="index">
          <td>{{item.ID}}</td>
          <td>{{item.Name}}</td>
          <td>{{item.Surname}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: "Leaderboard",
  data() {
    return {
      users: {},
      numberOfUsers: 0,
    };
  },
  async created(){
   const getUserData = await axios.get('https://sheet2api.com/v1/9OLQUnxSrqmQ/vue-sheets')
    .then(response => this.users = response.data);
    this.users = getUserData;
  }
};
</script>

<style scoped>
ul {
  list-style: none;
}
</style>
