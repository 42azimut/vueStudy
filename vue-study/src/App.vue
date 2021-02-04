<template>
<div>
  <h1>Hello {{ animal }} </h1>
  <h2> {{ animal }} loves a {{ food }}. </h2>
  <input type="text" v-model="food"/>
  <div v-html="alertMessage"></div>
  <div v-html="subscribeHTML"></div>
</div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      animal: "Monkey",
      food: "apple",
      alertMessage: "<h2>alert!</h2>",
      subscribeHTML: `<button onclick="document.querySelector('body').style.background = 'red'">구독하기!!</button>`
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
input {
  font-size: 20px;
}
</style>
