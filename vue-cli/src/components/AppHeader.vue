<template>
    <header>
        <h1>App Header</h1>
        <div>{{msg}}</div>
        <div>
            <button v-on:click="clickSend">click Send</button>
        </div>
    </header>
</template>

<script>
export default {
    events:{
        
    },

    data : function(){
        return {

        }
    },
    methods:{
        clickSend : function(){
            this.$emit('clicksend');
        }
    },

    props:{
        msg: String
    }
}
</script>

<style>

</style>