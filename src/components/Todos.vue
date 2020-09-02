<template>
  <div class="m-4">
    <div v-for="todo in todos" :key="todo.id">
      <TodoItem todo_prop.sync="todo"></TodoItem>
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
    todos_prop: {
      type: Array,
      default: () => [],
    },
  },
};
</script>