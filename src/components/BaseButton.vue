<template>
  <div class="btn-wrap">
    <button
      type="submit"
      :class="['iconfont', 'icon-' + icon]">{{ name }}</button>
  </div>
</template>

<script>
export default {
  name: "BaseButton",
  props: {
    name: {
      type: String,
      default: ""
    },
    icon: {
      type: String,
      default: ""
    },
  },
};
</script>

<style lang="less" scoped>
@import "../styles/mixins.less";
.btn-wrap {
  button {
    .btn-style();
  }
  button:active {
    .base-hover();
  }
}
</style>