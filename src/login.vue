<template>
  <div>
    <van-tabs
      @click="onClick"
      background="#07c160"
      title-active-color="pink"
      title-inactive-color="white"
      font-size="large"
    >
      <van-tab title="手机注册">
        <TelLogin> </TelLogin>
      </van-tab>
      <van-tab title="邮箱注册">
        <EmailLogin></EmailLogin>
      </van-tab>
    </van-tabs>
  </div>
</template>

<script>
import TelLogin from './components/TeleLogin.vue';
import EmailLogin from './components/EmailLogin.vue';

export default {
  methods: {
    onClick(name, title) {
      console.log(name, title);
    },
  },
  components: {
    TelLogin,
    EmailLogin,
  },
};
</script>

<style lang="less" scoped></style>
