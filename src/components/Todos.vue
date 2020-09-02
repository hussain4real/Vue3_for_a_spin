<template>
  <div class="m-4">
    <div v-for="todo in todos" :key="todo.id">
      <TodoItem :todo="todo"></TodoItem>
    </div>
  </div>
</template>

<script>
import TodoItem from "@/components/TodoItem.vue";
export default {
  name: "Todos",
  components: {
    TodoItem,
  },
  props: {
    todos: {
      type: Array,
      default: () => [],
    },
  },
};
</script>