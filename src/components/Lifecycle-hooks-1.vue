<script setup>
import { ref, onBeforeMount, onMounted, onUnmounted } from 'vue'

// En enkel ref för att demonstrera att komponenten renderas
const message = ref('Hello Vue!')

// Körs precis innan komponenten monteras i DOM:en
onBeforeMount(() => {
  console.log('LifecycleDemo: Komponenten förbereds')
})

// Körs när komponenten har monterats i DOM:en
// Här kan vi interagera med DOM:en säkert
onMounted(() => {
  console.log('LifecycleDemo: Komponenten är monterad')
})

// Körs när komponenten tas bort från DOM:en
// Perfekt för cleanup av t.ex. eventlisteners eller timers
onUnmounted(() => {
  console.log('LifecycleDemo: Komponenten är borttagen')
})
</script>

<template>
  <div class="lifecycle-demo">
    <h3>{{ message }}</h3>
  </div>
</template>

<style scoped>
.lifecycle-demo {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 4px;
}
</style> 