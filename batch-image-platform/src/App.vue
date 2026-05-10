<script setup lang="ts">
import { ref } from 'vue'

// ref = 响应式变量，类似 Python 的 self.count，但变了页面会自动刷新
const count = ref(0)

// 方法：点击时执行
const addOne = () => {
  count.value = count.value + 1
}
</script>


<template>
  <div class="box">
    <h1>批量图片生成平台</h1>
    <p class="number">当前计数：{{ count }}</p>
    <button @click="addOne">点我 +1</button>
  </div>
</template>

<style scoped>
.box {
  padding: 40px;
  text-align: center;
  font-family: 'Microsoft YaHei', sans-serif;
}
.number {
  font-size: 24px;
  color: #409eff;
  margin: 20px 0;
}
button {
  padding: 10px 24px;
  font-size: 16px;
  background: #409eff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button:hover {
  background: #66b1ff;
}
</style>