<template>
  <div class="dashboard-container">
    <div class="dashboard-text">Xyz66西宁野生动物园论坛后台</div>
    <div>
      欢迎关注Xyz的B站账号：<a href="https://space.bilibili.com/8443394"
        >https://space.bilibili.com/8443394</a
      >
      猫三棂
    </div>
    <div>Hello,World。</div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  name: "Dashboard",
  computed: {
    ...mapGetters(["name"]),
  },
};
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
