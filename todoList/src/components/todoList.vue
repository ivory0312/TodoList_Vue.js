<template>
  <div class="home">
    <div class="todo">
      <div class="todo-title">Todo List</div>
      <div class="todo-button">
        <input
          v-model="name"
          class="todo-button-input"
          type="text"
          @keypress.enter="createTodo(name)"
        />
        <button @click="createTodo(name)" class="todo-button-send">send</button>
      </div>
      <div class="todo-contents">
        <ul class="todo-contents-item">
          <li v-for="(todo, index) in todos" v-bind:key="todo">
            <span class="todo-contents-item-todos">{{ todo.name }}</span>
            <button @click="deleteTodo(index)" class="todo-contents-item-btn">
              X
            </button>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      todos: [
        {
          name: "할 일",
        },
      ],
    };
  },
  methods: {
    deleteTodo(index) {
      this.todos.splice(index, 1);
    },
    createTodo(name) {
      if (name != null) {
        this.todos.push({ name: name });
        this.name = null;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.todo {
  width: 300px;
  height: auto;
  margin: 50px auto;
  border: 1px solid #d2d2d2;
  justify-content: center;
  align-items: center;

  &-title {
    width: 100%;
    height: 40px;
    padding-top: 10px;
    background-color: #0067bc;
    color: white;
    font-size: 24px;
    text-align: center;
  }
  &-contents {
    &-item {
      &-todos {
        width: 100px;
        margin-right: 10px;
      }
      &-btn {
        background-color: none;
        border: none;
      }
    }
  }
  &-button {
    padding: 10px;
    border-bottom: 1px solid #d2d2d2;

    &-input {
      width: 220px;
      border: none;
    }
    &-input:focus {
      outline: none;
    }
    &-send {
      border: none;
      padding: 5px 10px;
      color: white;
      background-color: #0067bc;
    }
  }
}

li {
  list-style: none;
  margin: 10px 0;
}
</style>
