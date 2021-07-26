<template>
  <section>
    <Task v-for="task in tasks" :task="task" v-bind:key="task.index" :refresh="refresh" :id="tasks.indexOf(task)" />
  </section>
</template>

<script>
import Task from "./Task.vue";

export default {
  name: "TaskList",
  props: {
    tasks: Array,
    refresh: Function,
  },
  components: {
    Task,
  }
};
</script>

<style scoped>
section {
  width: 100%;
  padding: 20px;
}
</style>
