<script setup lang="ts">
import Versions from './components/Versions.vue'

const ipcHandle = () => window.electron.ipcRenderer.send('ping')
</script>

<template>
  <img alt="logo" class="logo" src="./assets/electron.svg" />
  <div class="creator">Powered by Lzx</div>
  <div class="text">
    新一代分布式版本控制工具
    <span class="vue">GitX</span>
    <!-- 基于
    <span class="ts">Git</span> -->
  </div>
  <p class="tip">基于开源<span class="ts">Git</span>分布式版本控制系统</p>
  <div class="actions">
    <div class="action">
      <a href="#" target="_blank" rel="noreferrer">快速开始</a>
    </div>
    <div class="action">
      <a target="_blank" rel="noreferrer" @click="ipcHandle">Github</a>
    </div>
  </div>
  <Versions />
</template>
