<template>
<div class="landing-page">
  <div id="app">
    <img src="./assets/timg.jpg" id="logo">
    <router-view/>
  </div>
</div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#logo{
  margin-top:60px;
  border-radius: 50px;
  border: 2px solid rgb(255, 255, 255) ;
  height: auto;
  width: 100px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 50px;
}
.landing-page{
  content:"";
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: url(./assets/background.jpg)no-repeat;
  background-size: cover;
}
</style>
