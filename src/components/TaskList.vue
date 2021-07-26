<template>
  <section>
    <Task />
    <Task />
    <Task />
    <Task />
  </section>
</template>

<script>
import Task from "./Task.vue";

export default {
  name: "TaskList",
  props: {
    task: [String],
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
