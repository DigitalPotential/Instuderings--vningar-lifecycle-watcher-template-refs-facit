<script setup>
import { ref, onMounted } from 'vue'

// Template ref för att få direkt tillgång till input-elementet
const inputRef = ref(null)

// När komponenten är monterad, fokusera input-fältet automatiskt
onMounted(() => {
  inputRef.value.focus()
})

// Funktion för att fokusera input-fältet när knappen klickas
const focusInput = () => {
  inputRef.value.focus()
}
</script>

<template>
  <div class="template-ref-demo">
    <!-- Bind template ref till input-elementet med ref="inputRef" -->
    <input 
      ref="inputRef"
      type="text" 
      placeholder="Detta fält ska fokuseras automatiskt"
    >
    <button @click="focusInput">Fokusera input</button>
  </div>
</template>

<style scoped>
.template-ref-demo {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 4px;
}

input {
  padding: 8px;
  margin-right: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  width: 300px;
}
</style> 