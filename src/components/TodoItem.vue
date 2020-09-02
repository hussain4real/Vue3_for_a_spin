<template>
  <div
    :class="{ 'line-through': todo.completed }"
    class="bg-gray-200 p-3 border border-gray-400 border-dotted"
  >
    <p>
      <input type="checkbox" v-on:change="markComplete" />
      {{todo.title}}
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: {
    todo: {
      type: Object,
      default: () => {},
    },
  },
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    },
  },
};
</script>