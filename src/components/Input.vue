<template>
  <input type="text" placeholder="Task" v-model="taskText" v-on:keydown="keydownHandler($event)" />
</template>

<script>
export default {
  name: 'Input',
  data() {
      return {
          taskText: '',
      }
  },
  props: {
      refresh: Function,
  },
  methods: {
      add() {
          const todoList = JSON.parse(localStorage.getItem("todoList"));
          if (todoList && todoList.length !== 0) {
              todoList.push(this.taskText);
              localStorage.setItem("todoList", JSON.stringify(todoList));
          } else {
              localStorage.setItem("todoList", JSON.stringify([this.taskText]));
          }
          this.refresh();
          this.taskText = '';
      },
      keydownHandler(e){
          if (e.keyCode === 13){
              this.add();
          }
      }
  }
}
</script>

<style scoped>
input {
  width: 90%;
  font-size: 1.6em;
  outline: none;
  border: none;
  border-bottom: 3px solid #ccc;
  background: #fff;
  padding: 10px;
}
input:focus {
  border-color: rgb(29, 165, 142);
}
</style>
