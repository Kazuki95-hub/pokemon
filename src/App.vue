<template>
  <div id="app">
    <button @click = "serch">検索</button>
    <p>検索結果:{{pokemon}}</p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data(){
    return {
      pokemon:""
    }
  },
  methods:{
    async serch(){
      let poke = await axios.get(`https://pokeapi.co/api/v2/type/4/`)
      console.log(poke);
      // this.pokemon= poke;
    }
  }
}
</script>