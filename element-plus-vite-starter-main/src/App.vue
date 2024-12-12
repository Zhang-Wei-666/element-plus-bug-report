<template>
  <el-config-provider namespace="ep" :z-index="3000">
    <RouterView />
  </el-config-provider>
</template>

<style>
#app {
  text-align: center;
  color: var(--ep-text-color-primary);
}
</style>
