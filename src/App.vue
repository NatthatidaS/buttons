<template>
  <div id="app">
    <div class="row">
      <div class="col-6">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Anodard_Pond_%28II%29.jpg/600px-Anodard_Pond_%28II%29.jpg" alt="">
         <CSbutton/>
      </div>
      <div class="col-6">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/85/Anodard_Pond_%28I%29.jpg/600px-Anodard_Pond_%28I%29.jpg" alt="">
         <CSbutton/>
      </div>
    </div>
    
  </div>
</template>

<script>
import CSbutton from './components/button'
export default {
  name: 'App',
  components: {
    CSbutton
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
</style>