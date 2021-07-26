<template>
  <input type="text" placeholder="Task" v-bind:value="task" />
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    task: String
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
