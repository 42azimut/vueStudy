<template>
<div>
  <h1>Hello {{ animal }} </h1>
  <h2> {{ animal }} loves a {{ food }}. </h2>
  <input type="text" v-model="food"/>
  <div v-html="alertMessage"></div>
  <div v-html="subscribeHTML"></div>
  <img v-bind:src="imageSource" alt="random"/>,
  <a :href="naverURL">{{ food }}</a>
  <hr>
  <h2 v-bind:class="{ red: food==='apple', 'not-good': food==='rice' }">원숭이는 {{ food }} 를 좋아 합니다.</h2>
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
      subscribeHTML: `<button onclick="document.querySelector('body').style.background = 'red'">구독하기!!</button>`,
      imageSource: "https://placeimg.com/100/100/any",
      naverURL: "https://www.naver.com",

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

.orange {
  color: orange;
}
.salmon {
  color: salmon;
}
.red {
  color: red;
}
.not-good {
  text-decoration: line-through;
}
</style>
