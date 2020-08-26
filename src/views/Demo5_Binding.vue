<template>
  <div id="demo5">
    <img v-bind:src="imageUrl" v-bind:height="height">
    <br><a :href="Onmylink">click this link</a>
    <div :class="[error,important]">array v-bind style</div>
    <div :class="[false ? error : '',important]">array v-bind style short if</div>
    <div :style="{color,fontSize}">array v-bind for style</div>
    <div :style="object">v-bind style object</div>

    <div :style="isActive ? styleObj : ''">v-bind style object with btn</div>
    <button @click="isActive = !isActive">Toggle Active</button>
  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return { //v-bind can chagne property of element for customize, short form :[property] , full form v-bind:[property] 
      imageUrl:"http://www.codemobiles.com/biz/images/codemobiles_10years_banner_home.jpg",
      height: 100,
      Onmylink: "https://www.youtube.com/watch?v=rqmEx4pGWzI&list=PLjPfp4Ph3gBry3sJDNrbqor5ikjwGDJ_7&index=12",
      error: "error_class",
      important: "important",
      color : "blue",
      fontSize: "30px",
      object:{
          backgroundColor:"yellow",
          color:"green"
      },
      styleObj:{
          backgroundColor:"green",
          color:"green"
      },
      isActive:false
    }
  },
};
</script>

<style>
.error_class{
    background-color: red;
    color : white;
}
.important{
    font-weight: 900;
}
</style>
