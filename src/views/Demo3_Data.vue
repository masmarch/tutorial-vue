<template>
  <h1>Data</h1>
  <button @click="count++; isLogged=true;">Count++</button>
  <span>{{count}}</span>
  <div>{{message}}</div>
  <div>{{isLogged}}</div>
    <input type="text" placeholder="Enter a message" v-model="message">
    <h2 v-if="isLogged">Yahoo mail!</h2>
    <div>{{account.username}} {{account.password}}</div>
    <div>{{courses[1]}}</div>
    <ul>
        <li v-for="(item,index) in courses" :key="index">{{item}}</li>
    </ul>
</template>

<script>
export default {
    name: "Demo3",
    mounted(){
        this.message = "Welcome back"
    },
    data() {
        return {
            count: 0,
            message: "",
            isLogged: false,
            account:{
                username : "march",
                password: "1234"
            },
            courses:[
                "Angular",
                "VueJS",
                "Fluter",
                "Lalavel"
            ]
        }
    }    
}
</script >

<style scoped>
li{
    background-color: aqua;
}
</style>