# vue-virt-list 虚拟列表 虚拟滚动列表

<p align="center">
  <a href="https://npmcharts.com/compare/vue-virt-list?minimal=true"><img src="https://img.shields.io/npm/dm/vue-virt-list.svg?sanitize=true" alt="Downloads"></a>
  <a href="https://www.npmjs.com/package/vue-virt-list"><img src="https://img.shields.io/npm/v/vue-virt-list.svg?sanitize=true" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue-virt-list"><img src="https://img.shields.io/npm/l/vue-virt-list.svg?sanitize=true" alt="License"></a>
</p>

<a href="./README.md" target="_blank">EN</a> | <a href="./README_cn.md" target="_blank">中文</a>

👉 <a href="https://d8diegi800.feishu.cn/wiki/MX2Vwn1RWiwUsokjhshcr6sVnNb?from=from_copylink" target="_blank">优势介绍</a>

## 文档

To check out docs, visit <a href="https://keno-lee.github.io/vue-virt-list/zh/" target="_blank">vue-virt-list</a>

## 快速开始

```shell
npm install vue-virt-list -S
```

### Options API

```html
<template>
  <div style="width: 500px; height: 400px">
    <VirtList itemKey="id" :list="list" :minSize="20">
      <template #default="{ itemData, index }">
        <div>{{ index }} - {{ itemData.id }} - {{ itemData.text }}</div>
      </template>
    </VirtList>
  </div>
</template>

<script>
  import { VirtList } from 'vue-virt-list';
  export default {
    components: { VirtList },
    data() {
      return {
        list: [{ id: 0, text: 'text' }],
      };
    },
  };
</script>
```

### Composition API

```html
<template>
  <div style="width: 500px; height: 400px">
    <VirtList itemKey="id" :list="list" :minSize="20">
      <template #default="{ itemData, index }">
        <div>{{ index }} - {{ itemData.id }} - {{ itemData.text }}</div>
      </template>
    </VirtList>
  </div>
</template>

<script setup lang="ts">
  import { VirtList } from 'vue-virt-list';

  const list = [{ id: 0, text: 'text' }];
</script>
```
