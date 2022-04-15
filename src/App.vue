<template>
  <div id="app">
    <compCard/>
  </div>
</template>
<script>
import compCard from './components/compCard.vue';

export default {
  name : 'app',
  components:{
    compCard
  }
}
</script>

<style>
#app {
  margin:0;
  padding:0;
  list-style:none;
  text-decoration: none;
  box-sizing: border-box;
}
</style>
