<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-transparent backdrop-blur-md">
  <div class="max-w-6xl mx-auto px-6 flex items-center justify-between h-16 relative z-10">
      
      <!-- Logo -->
      <span class="text-red-600 font-bold text-lg tracking-wide">
        Vanishaya
      </span>

      <!-- Desktop Menu -->
      <ul class="hidden sm:flex gap-8 list-none">
        <li><a href="#home"     class="text-red-600 hover:text-red-800 transition-colors text-sm">About me</a></li>
        <li><a href="#projects" class="text-red-600 hover:text-red-800 transition-colors text-sm">Projects</a></li>
        <li><a href="#skills"   class="text-red-600 hover:text-red-800 transition-colors text-sm">Skills</a></li>
        <li><a href="#contact"  class="text-red-600 hover:text-red-800 transition-colors text-sm">Contact</a></li>
      </ul>

      <!-- Hamburger Button (mobile only) -->
      <button
        class="sm:hidden flex flex-col gap-1.5 p-1 cursor-pointer items-center "
        @click="toggleMenu"
      >
        <span class="block w-6 h-0.5 bg-slate-400 transition-all"></span>
        <span class="block w-6 h-0.5 bg-slate-400 transition-all"></span>
        <span class="block w-6 h-0.5 bg-slate-400 transition-all"></span>
      </button>
    </div>

    <!-- Mobile Menu -->
    <ul
        v-if="isMenuOpen"
        class="sm:hidden flex flex-col gap-4 px-6 py-5 bg-transparent backdrop-blur-md border-t border-white/10 list-none items-center"
    >
      <li><a href="#home"     @click="isMenuOpen = false" class="text-red-600 hover:text-red-800 transition-colors">About me</a></li>
      <li><a href="#projects" @click="isMenuOpen = false" class="text-red-600 hover:text-red-800 transition-colors">Projects</a></li>
      <li><a href="#skills"   @click="isMenuOpen = false" class="text-red-600 hover:text-red-800 transition-colors">Skills</a></li>
      <li><a href="#contact"  @click="isMenuOpen = false" class="text-red-600 hover:text-red-800 transition-colors">Contact</a></li>
    </ul>
  </nav>
</template>

<style scoped></style>