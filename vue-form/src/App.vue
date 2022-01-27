<template>
    <div>
      <form action="" v-on:submit.prevent="loginSubmit">
        <div>
          <label for="username">id : </label>
          <input id="username" type="text" v-model="username" />
        </div>
        <div>
          <label for="password">password : </label>
          <input id="password" type="text" v-model="password"  />          
        </div>
        <div>
            <button type="submit" >Login</button>
        </div>
      </form>
    </div>
</template>

<script>

import axios from 'axios';

export default {

  data : function(){ 
    return{
      username : 'username',
      password : 'password' 
    } 
  },

  methods : {
    loginSubmit: function(){
        //event.preventDefault();

        console.log( this.username + '/' + this.password);
        console.log( this.data );

        const url = 'https://jsonplaceholder.typicode.com/users';
        const data = {
          username: this.username,
          password: this.password
        };

        axios.post(url, data)
        .then((response)=> console.log(response))
        .catch((err)=> console.log(err));
    }
  }


}
</script>

<style>

</style>