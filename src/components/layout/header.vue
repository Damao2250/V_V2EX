<template>
  <div class="header-nav">
    <div class="nav-v2ex">
      <div class="logo">V2EX</div>
      <div>
        <el-input
          class="search-value"
          v-model="searchValue"
          style="width: 240px"
        >
          <template #prefix>
            <el-icon class="el-input__icon"><search /></el-icon>
          </template>
        </el-input>
      </div>
    </div>
    <div class="nav">
      <span class="nav-item" v-for="nav in navs">{{ nav.title }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue"
const navs = ref([
  { title: "首页", url: "/" },
  { title: "damao2250", url: "/" },
  { title: "记事本", url: "/" },
  { title: "时间轴", url: "/" },
  { title: "设置 ", url: "/" },
  { title: "登出", url: "/" },
])
const searchValue = ref("")
</script>

<style lang="scss" scoped>
.header-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100%;
  background: #fff;
  width: 100%;
  padding: 0 50px;
  .nav-v2ex {
    display: flex;
    align-items: center;
    .logo {
      font-weight: bold;
      margin-right: 20px;
      font-size: 28px;
    }
    .search-value {
      :deep(.el-input__wrapper) {
        border-radius: 15px;
      }
    }
  }
  .nav {
    .nav-item {
      margin: 0 15px;
      cursor: pointer;
    }
  }
}
</style>
