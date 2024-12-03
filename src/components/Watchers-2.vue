<script setup>
import { ref, watch } from 'vue'

// Reaktiva variabler för formulärdata
const email = ref('')
const password = ref('')
const errors = ref({})

// Watch email för validering
watch(email, (newValue) => {
  if (!newValue.includes('@')) {
    errors.value.email = 'Email måste innehålla @'
  } else {
    delete errors.value.email
  }
})

// Watch password för validering
watch(password, (newValue) => {
  if (newValue.length < 6) {
    errors.value.password = 'Lösenord måste vara minst 6 tecken'
  } else {
    delete errors.value.password
  }
})
</script>

<template>
  <div class="form-demo">
    <div class="form-group">
      <input v-model="email" type="email" placeholder="Email">
      <span v-if="errors.email" class="error">{{ errors.email }}</span>
    </div>
    <div class="form-group">
      <input v-model="password" type="password" placeholder="Lösenord">
      <span v-if="errors.password" class="error">{{ errors.password }}</span>
    </div>
  </div>
</template> 