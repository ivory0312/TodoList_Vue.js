<template>
  <div class="todoItem">
    <input type="checkbox" name="" id="" />
    {{ msg }}
  </div>
</template>

<script>
import "./TodoItem.scss";

export default {
  name: "TodoItem",
  props: {
    msg: String,
  },
};
</script>
