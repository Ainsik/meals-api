<template>
  <header class="bg-white shadow h-16 flex justify-between items-stretch">
    <router-link
      :to="{ name: 'home' }"
      class="inline-flex items-center h-full px-5 text-orange-500 font-bold"
    >
      Home
    </router-link>
    <div class="flex items-center gap-1">
      <router-link
        :to="{ name: 'byName' }"
        class="hidden md:inline-flex items-center px-2 h-full transition-colors hover:bg-orange-500 hover:text-white"
      >
        Search Meals
      </router-link>
      <router-link
        :to="{ name: 'byLetter' }"
        class="hidden md:inline-flex items-center px-2 h-full transition-colors hover:bg-orange-500 hover:text-white"
      >
        Meals By Letter
      </router-link>
      <router-link
        :to="{ name: 'ingredients' }"
        class="hidden md:inline-flex items-center px-2 h-full transition-colors hover:bg-orange-500 hover:text-white"
      >
        Meals By Ingredients
      </router-link>
    </div>
    <div class="md:hidden flex items-center">
      <button @click="showMobileMenu = !showMobileMenu" class="p-5">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-8 h-8 hover:w-10 hover:h-10"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
          />
        </svg>
      </button>
    </div>
  </header>
  <div
    class="md:hidden text-right bg-white"
    :class="{ hidden: showMobileMenu }"
  >
    <router-link
      :to="{ name: 'byName' }"
      class="block px-5 py-2 hover:bg-orange-500 hover:text-lg"
      >Search Meals</router-link
    >
    <router-link
      :to="{ name: 'byLetter' }"
      class="block px-5 py-2 hover:bg-orange-500 hover:text-lg"
      >Meals By Letter</router-link
    >
    <router-link
      :to="{ name: 'ingredients' }"
      class="block px-5 py-2 hover:bg-orange-500 hover:text-lg"
      >Meals By Ingredients</router-link
    >
  </div>
</template>

<script setup>
import { ref } from "vue";

const showMobileMenu = ref(true);
</script>
