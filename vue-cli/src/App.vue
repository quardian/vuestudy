<template>
  <div>
    <h1>App</h1>
    <app-header 
      v-bind:msg="msg" 
      v-on:clicksend="clickSend"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
    data: function(){
      return {
        msg: 'hi!!',
        count: 0,
      }
    },
    methods: {
      clickSend: function(){
        this.count++;
        this.msg = "hi!!" + this.count;
      }
    },
    components:{
      'app-header': AppHeader
    }
}
</script>

<style>

</style>