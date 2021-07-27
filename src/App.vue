<template>
  <div id="app">
    <main>
      <Header/>
      <Input :refresh="refresh" />
      <TaskList :refresh="refresh" :tasks="todoList" />

      <div id="deleteAll">
        <span v-on:click="delAll()">Apagar Tudo</span>
      </div>
    </main>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Input from "./components/Input.vue";
import TaskList from "./components/TaskList.vue";

export default {
  name: 'App',
  components: {
    Header,
    Input,
    TaskList,
  },
  data(){
    return {
      todoList: JSON.parse(localStorage.getItem("todoList")) || []
    }
  },
  methods: {
    refresh() {
      const todoList = JSON.parse(localStorage.getItem("todoList"));
      if (todoList) {
        this.todoList = todoList;
      } else {
        this.todoList = [];
      }
    }, 
    delAll(){
      localStorage.removeItem("todoList");
      this.refresh();
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
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #222;
}
html, body {
  padding: 0;
  margin: 0;
}

main {
  border: 1px solid #ccc;
  border-radius: 3px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-direction: column;
  background: #fafafa;
  min-width: 60%;
}

#deleteAll {
  display: flex;
  align-self: center;
  justify-content: flex-end;
  flex-direction: row;
  width: 100%;
}
#deleteAll span {
  padding: 10px;
  text-decoration: underline;
  color: rgba(69, 134, 123, 0.835);
  cursor: pointer;
}

</style>
