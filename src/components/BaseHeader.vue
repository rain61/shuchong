<template>
  <header class="header">
    <div class="line">
      <div class="icon"></div>
      <search-bar />
      <div class="btn-group">
        <base-button :icon="'wode'" :name="'注册'" />
        <base-button :icon="'wode'" :name="'登录'" />
      </div>
    </div>
    <nav class="nav">
      <div class="nav-list">
        <router-link class="link" to="/">
          <div class="nav-item">首页</div>
        </router-link>

        <router-link class="link" to="/about">
          <div class="nav-item">关于</div>
        </router-link>

        <router-link class="link" to="#">
          <div class="nav-item">个人中心</div>
        </router-link>
      </div>
    </nav>
  </header>
</template>

<script>
import SearchBar from "../components/BaseSearchBar";
import BaseButton from "../components/BaseButton";

export default {
  components: {
    SearchBar,
    BaseButton
  }
};
</script>

<style lang="less" scoped>
@import "../styles/mixins.less";

.header {
  background: #fff;
  min-width: 900px;
  padding-top: 25px;
  .line {
    padding: 0 10%;
    margin-bottom: 6px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    .icon {
      min-width: 112px;
      height: 44px;
      background: url("../assets/images/favicon.png") no-repeat;
      background-size: 100% 100%;
    }
    .btn-group {
      display: flex;
      height: 40px;
      width: 174px;
      justify-content: space-between;
    }
  }
  .nav {
    padding: 0 10%;
    background: #4fb53d;
    min-width: 600px;
    height: 60px;
    display: flex;
    align-items: center;
    .nav-list {
      display: flex;
      justify-content: space-between;
      width: 280px;
      .link {
        color: #fff;
      }
      .nav-item {
        user-select: none;
        line-height: 60px;
        height: 60px;
        box-sizing: border-box;
        padding: 0 20px;

        text-align: center;
        a {
          color: #fff;
        }
        &:hover {
          background: rgba(63, 145, 29, 0.3);
        }
        &::before {
          width: 0;
          height: 100%;
          position: absolute;
          top: 0;
          left: 100%;
          border-bottom: 2px solid #000;
          content: "";
        }
      }
    }
  }
}
</style>