<template>
  <div id="demo2">
      <h1>Even and Method</h1>
      <button v-on:click="clickMe1">Click me1</button>
      <button v-on:click="clickMe2('Come Back')">Click me2</button>
      <button @click="clickMe3('to me!!')">Click me3</button>
    <h3>{{getTimestamp()}}</h3>
  </div>
</template>

<script>
export default {
    name:"demo2",
    mounted() {
        this.initial()
    },
    methods:{
        initial(){
            console.log("Initialization")
        },
        clickMe1(){
            alert("Hello World!!!")
        },
        clickMe2(message){
            alert(message)
        },
        clickMe3(message){
            alert(message)
        },
        getTimestamp(){
            return Date();
        }
    }
}
</script>

<style>

</style>