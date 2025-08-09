<script setup lang="ts">
definePageMeta({
  layout: 'card',
});
</script>

<template>
  <div
    class="min-h-(--full-height-page) flex items-center justify-center bg-gradient-to-br from-pink-200 via-purple-200 to-purple-300 p-6">
    <div class="bg-white rounded-2xl shadow-xl p-8 w-full max-w-md">
      <h1 class="text-3xl font-bold text-center text-purple-600 mb-6">
        🎉 Welcome 🎄
      </h1>
      <p class="text-center text-gray-700 mb-8">Choose a card to open:</p>

      <div class="flex flex-col gap-4">
        <NuxtLink
          to="/birthday/2025"
          class="bg-pink-500 hover:bg-pink-600 text-white py-3 px-6 rounded-lg shadow text-center font-semibold transition">
          Your 24th
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
