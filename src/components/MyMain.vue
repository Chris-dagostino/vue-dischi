<template>
  <main>
    <ListaDischi></ListaDischi>
  </main>
</template>

<script>
import ListaDischi from './ListaDischi.vue'
export default {
  name:'MyMain',
  components:{
    ListaDischi,
  },
  props:{
    
  }

}
</script>

<style lang="scss" scoped>
  main{
    background-color: #1e2d3a;
    height: 100vh;
  }

</style>