<template>
  <div class="home">
    <div class="home-title">Todo List</div>
    <TodoInput />
  </div>
</template>

<script>
// @ is an alias to /src
import TodoInput from "../components/TodoInput/TodoInput.vue";
import "./Home.scss";

export default {
  name: "Home",
  components: {
    TodoInput,
  },
};
</script>
