<template>
  <div class="hello">
    <h1>Welcome to Franky's blog</h1>
      <div id="content">
        <h2 id="acount">Acount:<input v-model="acount"  type="text" value=""  ></h2>
        <h2>Password:<input v-model="password"  type = "password" ></h2>
      </div>
      <a v-on:click="SignIn" href="" >Sign in</a>
  </div>
</template>

<script>
export default {
  name: 'SignIn',
  data () {
    return {
      password: '',
      acount: ''
    }
  },
  methods: {
    SignIn: function () {
      this.$http.post('http://localhost:3000/SignIn', {
        acount: this.acount,
        password: this.password
      }).then(function (data) {
        alert(data)
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
