<script setup>
import { ref, watch } from 'vue'

// Reaktiv räknare
const count = ref(0)

// Watch som övervakar ändringar i count
// Loggar både gamla och nya värdet när count ändras
watch(count, (newValue, oldValue) => {
  console.log(`WatcherDemo: Count ändrades från ${oldValue} till ${newValue}`)
})
</script>

<template>
  <div class="watcher-demo">
    <h3>Count: {{ count }}</h3>
    <div class="button-group">
      <button @click="count++">Öka</button>
      <button @click="count--">Minska</button>
    </div>
  </div>
</template>

<style scoped>
.watcher-demo {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 4px;
}

.button-group {
  display: flex;
  gap: 10px;
}
</style> 