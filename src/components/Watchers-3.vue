<script setup>
import { ref, watch } from 'vue'

// Reaktiva variabler för text och ordräkning
const text = ref('')
const wordCount = ref(0)

// Watch som räknar ord när texten ändras
watch(text, (newValue) => {
  // Dela upp texten på whitespace och filtrera bort tomma strängar
  const words = newValue.trim().split(/\s+/).filter(word => word.length > 0)
  wordCount.value = words.length
})
</script>

<template>
  <div class="text-counter">
    <div class="input-group">
      <label for="text-input">Skriv din text:</label>
      <textarea 
        id="text-input"
        v-model="text" 
        placeholder="Börja skriva här..."
        rows="4"
      ></textarea>
    </div>
    <p class="word-count">Antal ord: {{ wordCount }}</p>
  </div>
</template>

<style scoped>
.text-counter {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
}

.input-group {
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin-bottom: 16px;
}

label {
  font-weight: bold;
  color: #333;
}

textarea {
  padding: 12px;
  border: 1px solid #ddd;
  border-radius: 4px;
  resize: vertical;
  min-height: 100px;
  font-family: inherit;
}

.word-count {
  font-size: 1.1em;
  color: #2c3e50;
  margin: 0;
}
</style> 