<template>
  <div>
    <slot name="area">
      <van-radio-group
        v-model="radio"
        direction="horizontal"
        style="padding: 20px 0 30px 50px"
      >
        <van-radio name="1" style="margin-right: 80px">中国大陆</van-radio>
        <van-radio name="2">中国香港</van-radio>
      </van-radio-group>
    </slot>
    <slot name="email">
      <van-field
        v-model="email"
        type="email"
        label="邮箱地址"
        placeholder="输入邮箱地址"
      />
      <van-field
        v-model="sms"
        center
        clearable
        label="邮箱验证码"
        placeholder="输入验证码"
      >
        <van-button size="small" type="primary">发送验证码</van-button>
      </van-field>
    </slot>
    <slot name="password">
      <van-field
        v-model="password"
        type="password"
        label="密码"
        placeholder="输入登录密码"
      />
      <van-field
        v-model="rePassword"
        type="password"
        placeholder="再次输入登录密码"
        label="再次输入密码"
      />
    </slot>
    <slot name="other">
      <van-field
        v-model="inviteCode"
        type="password"
        placeholder="输入客户经理邀请码"
        label="邀请码(选填)"
      />
    </slot>
    <slot name="login">
      <van-button type="primary" size="large">邮箱注册</van-button>
    </slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      radio: '1',
      email: '',
      sms: '',
      password: '',
      rePassword: '',
      inviteCode: '',
    };
  },

  mounted() {},

  methods: {},
};
</script>
