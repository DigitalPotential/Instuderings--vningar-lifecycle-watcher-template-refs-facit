<script setup>
import { ref, onMounted } from 'vue'

// Array för att hålla alla input-referenser
const inputs = ref([])
// Håll reda på vilket input som är aktivt
const currentIndex = ref(0)

// Flytta fokus till nästa input när Enter trycks
const focusNext = () => {
  if (currentIndex.value < inputs.value.length - 1) {
    currentIndex.value++
    inputs.value[currentIndex.value].focus()
  }
}

// Fokusera första input-fältet när komponenten monteras
onMounted(() => {
  inputs.value[0].focus()
})
</script>

<template>
  <div class="input-demo">
    <!-- Skapa tre input-fält och spara referens till varje -->
    <input 
      v-for="(_, index) in 3" 
      :key="index"
      :ref="el => inputs[index] = el"  <!-- Dynamisk ref-binding -->
      @keyup.enter="focusNext"
      :placeholder="`Input ${index + 1}`"
    >
  </div>
</template> 