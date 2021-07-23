<template>
  <h1>{{name}}</h1>
  <div class="row">
    <div class="col-lg-4 col-md-6 col-sm-6 col-6 player" v-for="player in roster" :key='player'>
      <img :src="player.image" class="img-fluid">
      <h3>{{player.name}}</h3>
      <h5>{{player.position}}</h5>
      <p v-if="player.status === true">Healthy</p>
      <p v-else>Not Available</p>
    
  </div>
  </div>
</template>

<script>


import "bootstrap/dist/css/bootstrap.min.css";

export default {
  name: 'App',
  data() {
    return {
      name: 'Milwaukee Bucks 2020-2021 Roster',
      roster: [
        {name: 'Giannis Antetokoumpo', position: 'Power Forward', rating: "Franchise Superstar", status: true, image: "assets/bucks-greekfreak.png"},
        {name: 'Khris Middleton', position: 'Shooting Guard', rating: "All Star Reserve", status: true, image: "assets/bucks-khris.png"},
        {name: 'Jrue Holliday', position: 'Point Guard', rating: "All-NBA Defender", status: true, image: "assets/bucks-jrue.png"},
        {name: 'Bobby Portis', position: 'Small Forward', rating: "Emotional Uplifter", status: true, image: "assets/bucks-bobby.png"},
        {name: 'Brook Lopez', position: 'Center', rating: "Inside Big", status: true, image: "assets/bucks-brook.png"},
        {name: 'P.J. Tucker', position: 'Center', rating: "Do Dirty Work", status: true, image: "assets/bucks-pj.png"},
        {name: 'Pat Connaughton', position: 'Shooting Guard', rating: "Dunk and Hops", status: true, image: "assets/bucks-pat.png"},
        {name: 'Donte DiVincenzo', position: 'Shooting Guard', rating: "Hops and Shoot", status: false, image: "assets/bucks-donte.png"}
      ]
    }
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

.player {
  background: green;
}
</style>
