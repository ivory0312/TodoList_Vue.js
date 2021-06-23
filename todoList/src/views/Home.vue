<template>
  <div class="home">
    <div class="home-title">2020년도 웹 프로그래밍 수업 과제</div>
    <Main />
  </div>
</template>

<script>
import Main from "../components/Main.vue";

export default {
  name: "home",
  components: { Main },
};
</script>

<style lang="scss" scoped>
.home {
  margin: 50px auto;
  width: 300px;

  &-title {
    text-align: center;
  }
}
</style>
