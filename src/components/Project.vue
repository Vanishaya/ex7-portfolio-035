<script setup>
import { ref } from 'vue'
import travel from '../assets/travel.jpg'

const projects = ref([
  {
    title: 'Travel Quest',
    description: 'A gamified travel recommendation platform. Features a social feed and a custom "Accept Quest" system to reward users for exploring.',
    image: travel,
    tags: ['Vue.js', 'Tailwind CSS', 'UX/UI'],
  }
])
</script>

<template>
  <section id="projects" class="min-h-screen px-6 py-24 relative overflow-hidden">

    <div class="max-w-6xl mx-auto relative z-10 ">

      <!-- Header -->
      <div class="mb-16">
        <h2 class="text-5xl font-bold text-stone-900">
          Pro<span class="text-red-700">jects</span>
        </h2>
      </div>

      <!-- Project Cards -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 ">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="group rounded-2xl overflow-hidden border border-stone-200 hover:border-red-200 hover:shadow-lg hover:shadow-red-100 transition-all duration-300 hover:-translate-y-1 bg-white/40 backdrop-blur-sm"
        >
          <!-- Image -->
          <div class="overflow-hidden h-48">
            <img
              :src="project.image"
              :alt="project.title"
              class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
            />
          </div>

          <!-- Content -->
          <div class="p-5">
            <h3 class="font-bold text-stone-900 text-lg mb-2">{{ project.title }}</h3>
            <p class="text-stone-400 text-sm leading-relaxed mb-4">{{ project.description }}</p>

            <!-- Tags -->
            <div class="flex flex-wrap gap-2">
              <span
                v-for="tag in project.tags"
                :key="tag"
                class="text-xs px-3 py-1 rounded-full bg-red-50 text-red-700 border border-red-100"
              >
                {{ tag }}
              </span>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped></style>