<script lang="ts" setup>
import { icons } from '@element-plus/icons-vue/global'
console.log(icons)
</script>

<template>
  <ul class="icon-list">
    <div v-for="(Icon, key) in icons" :key="key" class="icon-item">
      <span class="svg-icon">
        <component :is="Icon" class="icon" />
        <p>{{ key }}</p>
      </span>
    </div>
  </ul>
  <!-- <component
    :is="`ElIcon${key}`"
    v-for="key in Object.keys(icons)"
    :key="key"
    class="icon"
  /> -->
</template>

<style>
body {
  font-family: Inter,Helvetica Neue,Helvetica,PingFang SC,Hiragino Sans GB,Microsoft YaHei,\5fae\8f6f\96c5\9ed1,Arial,sans-serif;
}
.icon {
  height: 48px;
  color: #409eff;
}
.icon-list {
  --el-border-color: #dcdfe6;
  --el-text-color-regular: #606266;
  --el-transition-duration: .3s;
}
.icon-list {  
  list-style: none;
  padding: 0 !important;
  border-top: 1px solid var(--el-border-color);
  border-left: 1px solid var(--el-border-color);
  border-radius: 4px;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  
}

.svg-icon {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  cursor: pointer;
}

.icon-item {
  text-align: center;
  color: var(--el-text-color-regular);
  height: 90px;
  font-size: 13px;
  border-right: 1px solid var(--el-border-color);
  border-bottom: 1px solid var(--el-border-color);
  transition: background-color var(--el-transition-duration);
}
p {
  margin: 0;
}
</style>
