<template>
  <div class="layout">
    <Header class="layout-header" />
    <div class="layout-view">
      <RouterView />
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from "@/components/layout/header.vue"
</script>

<style lang="scss" scoped>
.layout {
  display: flex;
  flex-direction: column;
  .layout-header {
    height: 50px;
  }
  .layout-view {
    height: calc(100vh - 50px);
    background: #e2e2e2;
  }
}
</style>
