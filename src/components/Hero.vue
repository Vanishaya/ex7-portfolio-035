<script setup>
import profile from '../assets/VBS.jpg'
</script>

<template>
  <section id="home" class="min-h-screen flex items-center justify-center px-6 pt-24 pb-16 relative overflow-hidden">

    <div class="max-w-6xl mx-auto w-full flex flex-col-reverse sm:flex-row items-center justify-between gap-12 relative z-10">

      <!-- Text Side -->
      <div class="flex-1 text-center sm:text-left">

        <!-- Name -->
        <h1 class="font-bold text-stone-900 leading-tight mb-2 text-7xl" >
          Vanishaya<br>
          <span class="text-red-700">Saephu</span>
        </h1>

        <!-- Bio -->
        <p class="text-stone-400 text-sm leading-relaxed max-w-md mb-10 mt-6">
          Currently studying Information Technology at King Mongkut's University of Technology Thonburi (KMUTT), 
          2nd year student .
        </p>

      </div>

      <!-- Image Side -->
      <div class="flex-shrink-0 ">
        <div class="w-48 h-48 sm:w-56 sm:h-56 rounded-full p-[3px]"
             style="background: linear-gradient(135deg, #b91c1c, #fca5a5)">
          <div class="w-full h-full rounded-full bg-amber-100 flex items-center justify-center text-7xl">
            <img :src="profile" class="w-full h-full rounded-full object-cover object-top" />
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped></style>
