<template>
  <div class="main">
    <div class="main-left">
      <div class="main-left-dot" />
      <div class="main-left-line" />
    </div>
    <div class="main-right">
      <span class="main-right-text">hi</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "main",
};
</script>

<style lang="scss" scoped>
.main {
  width: 300px;
  margin-top: 30px;
  padding: 15px;

  &-left {
    float: left;
    width: 30px;

    &-dot {
      width: 10px;
      height: 10px;
      margin-top: 4px;
      border-radius: 100px;
      background-color: #0067bc;
    }
    &-line {
      height: 40px;
      margin-left: 4px;
      border-left: 2px solid #0067bc;
    }
  }
  &-right {
    float: left;
    width: 270px;
  }
}
</style>
