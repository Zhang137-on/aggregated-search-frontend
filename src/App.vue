<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
body {
  margin: 0;
  display: flex;
  justify-content: center;
  padding-top: 40px; /* 距离顶部 20px */
  background: #f5f5f5; /* 可选：添加背景色 */
}

#app {
  max-width: 1024px;
  width: 100%;
  padding-bottom: 20px;
}
</style>

<script setup lang="ts"></script>
