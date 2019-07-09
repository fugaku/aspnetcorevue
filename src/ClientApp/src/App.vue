<template>
  <div id="app" :style="{ background: 'blue', height: 'calc(100vh - 55px)' }">
    <a-layout id="top-layout" style="min-height: 100vh">
      <a-layout-sider collapsible v-model="collapsed">
        <div class="logo">AkuntingKU</div>>
        <a-menu theme="dark" :defaultSelectedKeys="['1']" mode="inline">
          <a-menu-item key="1">
            <a-icon type="home" />
            <span>Home</span>
          </a-menu-item>
          <a-menu-item key="2">
            <a-icon type="profile" />
            <span>Tipe Akun</span>
          </a-menu-item>
          <a-menu-item key="3">
            <a-icon type="bank" />
            <span>Akun</span>
          </a-menu-item>
          <a-menu-item key="4">
            <a-icon type="project" />
            <span>Jurnal</span>
          </a-menu-item>
          <a-menu-item key="9">
            <a-icon type="setting" />
            <span>Konfigurasi</span>
          </a-menu-item>
        </a-menu>
      </a-layout-sider>
      <a-layout>
        <a-layout-header style="background: #fff; padding: 0" />
        <a-layout-content style="margin: 0 16px">
          <a-breadcrumb style="margin: 16px 0">
            <a-breadcrumb-item>User</a-breadcrumb-item>
            <a-breadcrumb-item>Bill</a-breadcrumb-item>
          </a-breadcrumb>
          <div :style="{ padding: '24px', background: '#fff', minHeight: '360px' }">Bill is a cat.</div>
        </a-layout-content>
        <a-layout-footer style="text-align: center">AkuntingKU © 2019</a-layout-footer>
      </a-layout>
    </a-layout>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";

@Component({
  components: {
    HelloWorld
  }
})
export default class App extends Vue {
  data() {
    return {
      collapsed: false
    };
  }
}
</script>

<style>
#top-layout .logo {
  height: 32px;
  margin: 16px;
  font-size: 20px;
  color: white;
  text-align: center;
}
</style>
