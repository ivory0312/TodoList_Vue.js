<template>
  <div class="main">
    <div class="main-left">
      <div class="main-left-dot" />
      <div class="main-left-line" />
      <div class="main-left-dot" />
      <div class="main-left-line" />
      <div class="main-left-dot" />
      <div class="main-left-line" />
      <div class="main-left-dot" />
    </div>
    <div class="main-right">
      <div class="main-right-text">2021.06.08 프로젝트 계획서 쓰기</div>
      <div class="main-right-text">2021.06.16 계속 미루기</div>
      <div class="main-right-text">2021.06.17 프로젝트 생성</div>
      <div class="main-right-text">2021.06.23 Todo List 완성</div>
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

    &-text {
      margin-bottom: 30px;
    }
  }
}
</style>
