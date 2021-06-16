<template>
  <div class="todoInput">
    <TodoItem msg="hi" />
    <input class="todoInput-text" type="text" />
    <button @click="addTodo" class="todoInput-btn">send</button>
  </div>
</template>

<script>
import TodoItem from "../TodoItem/TodoItem.vue";
import "./TodoInput.scss";

export default {
  name: "TodoInput",
  components: {
    TodoItem,
  },
  // method: {
  //   state: {
  //     message: "",
  //   },
  //   setMessage(value) {
  //     this.state.message = value;
  //     console.log(this.state.message);
  //   },
  //   removeMessage() {
  //     this.state.message = "";
  //   },
  // },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const todo = {
        text: document.querySelector("todoInput-text").value,
        completed: false,
      };
      this.todos.push(todo);
      console.log(todo);
    },
  },
};
</script>
