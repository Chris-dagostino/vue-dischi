<template>
  <div class="contDischi" >
    <div class="container" >
      <div class="row" >

        <div class="col" v-for="(disco,index) in listaDischi"  :key="index">
          <div class="card" >
            <img :src="disco.poster" alt="poster">
            <h1 class="nomeDisco" >{{disco.title}}</h1>
            <div class="artista" >{{disco.author}}</div>
            <div class="anno" >{{disco.year}}</div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>

  const axios = require('axios');

  export default {
    name:'ListaDischi',

      data (){
        return{
          listaDischi: []
        }
      },

      methods:{
        arrayDischi(){
          axios.get('https://flynn.boolean.careers/exercises/api/array/music')
          .then((response)=> {
            console.log(response);
            this.listaDischi = response.data.response;
          })
          .catch(function (error) {
            // handle error
            console.log(error);
          });
        }
      },
      created(){
        this.arrayDischi()
      }
      
  }

</script>

<style lang="scss" scoped>

  .contDischi{
    width: 80%;
    height: 100vh;
    margin: auto;
    .card{
      text-align: center;
      padding: 20px;
      background-color: #2e3a46;
      width: 200px;
      height: 350px;
      margin: 20px;
      h1{
        font-size: 20px;
        margin: 10px 0px;
      }
      .nomeDisco{
        color: #fff;
      }
      .artista, .anno {
        color: #868686;
      }
    }
  }
  

</style>