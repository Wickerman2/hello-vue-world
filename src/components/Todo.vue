<template>
  <div>
    <div v-for="todo in todos" :key="todo.id">
      <TodoItem :todo="todo" @del-todo="$emit('del-todo', todo.id)" />
    </div>
  </div>
</template>
<script>
import axios from "axios";
import TodoItem from "./TodoItem.vue";

export default {
  name: "Todo",
  components: {
    TodoItem
  },
  data() {
    return {
      todos: null
    };
  },
  mounted: function() {
      axios
        .get("https://jsonplaceholder.typicode.com/todos?_limit=10")
        .then(res => (this.todos = res.data))
        .catch(() => (this.todos = []));
  },
};
</script>

<style></style>
