<template>
  <header>
    <div class="logo" >
      <h1>Spotify</h1>
    </div>
  </header>
</template>

<script>
export default {
  name:'MyHeader',
  data (){
    return{

    }
  }
}
</script>

<style lang="scss" scoped>
  header{
    width: 100%;
    height: 100px;
    background-color: #2e3a46;
    display: flex;
    h1{
      color: #fff;
      align-content: center;
    }
  }

</style>