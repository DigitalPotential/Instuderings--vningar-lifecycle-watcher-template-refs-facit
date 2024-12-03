<script setup>
import WatchCount from './components/Watchers-1.vue'
import FormWatcherDemo from './components/Watchers-2.vue'
import TemplateRefDemo from './components/Template-refs-1.vue'
import TextCounter from './components/Watchers-3.vue'
import LifecycleDemo from './components/Lifecycle-hooks-1.vue'
import TemplateRefDemo2 from './components/Template-refs-2.vue'
import { ref } from 'vue'

const showLifecycleDemo = ref(true)
</script>

<template>
  <div class="container">
    <h1>Vue Lifecycle, Watchers & Template refs Demo</h1>
    
    <section>
      <h2>Lifecycle Hooks</h2>
      <button @click="showLifecycleDemo = !showLifecycleDemo">
        {{ showLifecycleDemo ? 'Ta bort' : 'Visa' }} komponenten
      </button>
      <LifecycleDemo v-if="showLifecycleDemo" />
    </section>

 

    <section>
      <h2>Template Ref 1 Demo</h2>
      <TemplateRefDemo />
    </section>

    <!-- <section>
      <h2>Template Ref 2 Demo</h2>
      <TemplateRefDemo2 />
    </section> -->

    <section>
      <h2>Watcher 1 Demo</h2>
      <WatchCount />
    </section>

    <section>
      <h2>Watcher 2 Demo</h2>
      <FormWatcherDemo />
    </section>

    <section>
      <h2>Watcher 3 Demo</h2>
      <TextCounter />
    </section>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

section {
  margin: 20px 0;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
}

button {
  margin: 10px 0;
  padding: 8px 16px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}
</style>
