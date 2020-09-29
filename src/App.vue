<template>
  <div id="app">
    <a-layout id="components-layout-demo-top" class="layout">
      <a-layout-header>
        <div class="logo" />
        <a-menu
          theme="dark"
          mode="horizontal"
          :default-selected-keys="['home']"
          :style="{ lineHeight: '64px' }"
        >
          <a-menu-item key="home">
            <router-link :to="{ name: 'home'}">Home</router-link>
          </a-menu-item>
          <a-menu-item key="login">
            <router-link :to="{ name: 'login'}">Login</router-link>
          </a-menu-item>
          <a-menu-item key="register" style="align-items: right;" class="register">
            <router-link :to="{ name: 'register'}">Register</router-link>
          </a-menu-item>
        </a-menu>
      </a-layout-header>
      <a-layout-content style="padding: 0px 0px">
        <div :style="{ background: '#fff', padding: '50px 100px', minHeight: '100vh' }">
          <router-view/>
        </div>
      </a-layout-content>
      <a-layout-footer style="text-align: center">
        Ant Design ©2018 Created by Ant UED
      </a-layout-footer>
    </a-layout>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#components-layout-demo-top .logo {
  width: 120px;
  height: 31px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px 24px 16px 0;
  float: left;
}
</style>
