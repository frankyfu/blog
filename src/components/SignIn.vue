<template>
  <div class="hello">
    <h1>Welcome to Franky's blog</h1>
      <div id="content">
        <h2 id="acount">Acount:<input v-model="user.acount"  type="text"  ></h2>
        <h2>Password:<input v-model="user.password"  type = "password" ></h2>
      </div>
      <a v-on:click="SignIn" href="#" >Sign in</a>
      <h1>{{acount}}
      {{password}}</h1>
  </div>
</template>

<script>
export default {
  name: 'SignIn',
  data () {
    return {
      user: {
        password: '',
        acount: ''
      }
    }
  },
  methods:{
    SignIn:function(){
      
      this.$http.post("",{
        acount:this.user.acount,
        password:this.user.password
      }).then(function(data){
        console.log(data)
      })
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,h2 {
  font-weight: normal;
}
#acount{
  margin-left: 30px;
}
input{
  background-color: white;
  border: solid 2px black;
  height: 25px;
  width: 200px;
  font-size: 20px;
  margin-left: 10px;
}
a{
  font-size: 23px;
  color: black;
  display: inline-block;
  text-decoration: none ;
  border: solid 2px black;
  padding:3px;
  border-radius: 4px;
}
</style>
