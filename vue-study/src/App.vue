<template>
<div>
  <h2>Your age is {{ age }}.</h2>
  <h3 v-if="age > 18">You are an adult.</h3>
  <h3 v-else-if="age > 13 && age <= 18">당신은 청소년 입니다.</h3>
  <h3 v-else>당신은 미성년자 입니다!</h3>
  <div>
    <h2 v-if="display">v-if display보입니다!!</h2>
    <h2 v-show="display">v-show 보입니다!!</h2>
  </div>
  <hr/>
  
  <div>
    <template v-for="(animal, index) in animals" :key="index">
      <h2 v-if="animal !=='monkey'">index: {{ index }} is {{ animal }}</h2>
    </template>
  <hr/>


    <ul>
      <li v-for="(user, idx) in users" :key="idx">{{ user.name }}의 직업은 {{ user.job }}
        <p v-for="item in user.skill" :key="item">{{ item }}</p>
      </li>
    </ul>
  </div>
</div>

</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      age : 14,
      display: true,
      animals: ["monkey", "rat", "dog", "lion", "monkey"],
      users: [
        { name: "'jayden", job: "developer", gender: "male", skill: ["vue", "js", "python"]},
        { name: "'kay", job: "singer", gender: "female", skill: ["html", "css", "ai"] },
        { name: "'iu", job: "model", gender: "female", skill: ["c", "pytorch", "tensorflow"]},
      ]
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
