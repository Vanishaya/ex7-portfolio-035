<script setup>
import { ref } from 'vue'

const Frontend = ref([
  { name: 'Vue.js'},
  { name: 'HTML/CSS'},
  { name: 'JavaScript'},
  { name: 'Tailwind CSS'},
])

const Backend = ref([
  { name: 'Node.js'},
  { name: 'Express.js'},
  { name: 'MySQL'},
])

const Tools = ref([
  { name: 'GitHub'},
  { name: 'VS Code'},
])
</script>

<template>
  <section id="skills" class="min-h-screen px-6 py-24 relative overflow-hidden">
    <div class="max-w-6xl mx-auto relative z-10">

      <!-- Section Title -->
      <div class="mb-16">
        <h2 class="text-5xl font-bold text-stone-900">
          S<span class="text-red-700">kills</span>
        </h2>
      </div>

      <!-- Skills Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-3 gap-8">

        <div
          v-for="category in [{ label: 'Frontend', items: Frontend }, { label: 'Backend', items: Backend }, { label: 'Tools', items: Tools }]"
          :key="category.label"
          class="rounded-2xl border border-stone-200 bg-white/40 backdrop-blur-sm p-6 hover:border-red-200 hover:shadow-lg hover:shadow-red-100 transition-all duration-300"
        >
          <h3 class="font-bold text-stone-900 text-lg mb-5 pb-3 border-b border-stone-100">
            {{ category.label }}
          </h3>

          <div class="flex flex-col gap-3">
            <div
              v-for="skill in category.items"
              :key="skill.name"
              class="flex items-center gap-3 group"
            >
              <span class="w-1.5 h-1.5 rounded-full bg-red-400 group-hover:bg-red-700 transition-colors flex-shrink-0"></span>
              <span class="text-stone-600 text-sm group-hover:text-stone-900 transition-colors">
                {{ skill.name }}
              </span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped>

</style>