<template>
  <div class="hello">
    <h1>{{ msg + "ddd" }}</h1>
    <p v-if="isShow">이제 나를 볼 수 있어요</p>
    <p v-for="(todo, i) in todos" v-bind:key="i">{{ todo.text }}</p>
    <button v-on:click="reverseMessage">메시지 뒤집기</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      isShow: true,
      todos: [
        { id: 1, text: "JavaScript 배우기" },
        { id: 2, text: "Vue 배우기" },
        { id: 3, text: "무언가 멋진 것을 만들기" },
      ],
    };
  },
  methods: {
    reverseMessage() {
      this.msg = this.msg.split("").reverse().join("");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
