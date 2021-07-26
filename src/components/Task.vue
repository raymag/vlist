<template>
  <article>
      <span>Clear Room</span>
      <button>x</button>
    </article>
</template>

<script>
export default {
  name: 'Task',
  props: {
    task: String
  }
}
</script>

<style scoped>
article {
  margin: auto;
  width: 90%;
  margin: 20px auto;
  margin-bottom: 0;
  border: solid 1px #ddd;
  border-radius: 3px;
  padding: 10px;
  background: #fff;
  display: flex;
  align-self: center;
  justify-content: space-between;
  font-size: 1.2em;
}
article button {
  border: none;
  background: none;
  font-weight: bold;
  font-size: 1.2em;
  color: rgb(165, 29, 29);
  cursor: pointer;
}
article button:hover {
  color: rgb(246, 36, 36);
}
article button:active {
  transform: translate(0, 2px);
}
article span {
  align-self: center;
}
</style>
