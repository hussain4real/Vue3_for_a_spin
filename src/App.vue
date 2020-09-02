<template>
  <div>
    <Todos todos_prop.sync="todos"></Todos>
  </div>
</template>

<script>
import Todos from "@/components/Todos.vue";
export default {
  name: "App",
  components: {
    Todos,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "first todo",
          completed: false,
        },
        {
          id: 2,
          title: "second todo",
          completed: true,
        },
        {
          id: 3,
          title: "third todo",
          completed: false,
        },
      ],
    };
  },
};
</script>

