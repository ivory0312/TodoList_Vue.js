<template>
  <div class="home">
    <div class="todo">
      <div class="todo-title">Todo List</div>
      <div class="todo-contents">
        {{ input }}
      </div>
      <div class="todo-button">
        <input v-model="input" class="todo-button-input" type="text" />
        <button v-on:click="send()" class="todo-button-send">send</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      input: "",
      list: [],
    };
  },
  method: {
    send: function() {
      this.list.push(input);
    },
  },
};
// console.log(data().input);
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
    padding: 10px;
  }
  &-button {
    padding: 10px;
    border-top: 1px solid #d2d2d2;

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
</style>
