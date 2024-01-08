<template>
  <div class="dashboard-container">
    <div class="dashboard-text">猫三棂<br>西宁野生动物园论坛后台</div>
    <div>
      欢迎关注Xyz的B站账号:<a href="https://space.bilibili.com/8443394"
        >https://space.bilibili.com/8443394</a
      >
    </div>
    <div>Hello,World。<br>欢迎您！{{ this.userInfo.user.nickName }}</div>
  </div>
</template>

<script>
import { getInfo } from "@/api/login";
import user from "@/store/modules/user";
import { mapGetters } from "vuex";
export default {
  name: "Dashboard",
  data(){
    return{
      userInfo:""
    }
  },
  methods: {
    getInfo() {
      getInfo().then((response) => {
        this.userInfo = response;
        console.log(this.userInfo.user.nickName);
      });
    },
  },
  computed: {
    ...mapGetters(["name"]),
  },
  created(){
    this.getInfo();
  }
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
