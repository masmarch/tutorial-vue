<template>
  <div id="demo1">
    <h1>Demo:v-moel</h1>
    <input v-model="message" type="text" placeholder="Enter your message" />
    <br><span>{{ message }}</span>
  </div>
  <button @click="message = ''">Reset</button>
</template>

<script>
export default {
  name: "demo1",
  data() {
    return {
      message: "",
    };
  },
};
</script>

<style></style>
