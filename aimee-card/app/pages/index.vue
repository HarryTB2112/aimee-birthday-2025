<template>
  <div
    class="min-h-screen flex items-center justify-center bg-gradient-to-br from-pink-200 via-purple-200 to-purple-300 p-6">
    <div class="bg-white rounded-2xl shadow-xl p-8 w-full max-w-md">
      <h1 class="text-3xl font-bold text-center text-purple-600 mb-6">
        🎉 Welcome Aimée
      </h1>
      <p class="text-center text-gray-700 mb-8">Choose an occasion:</p>

      <div class="flex flex-col gap-4">
        <NuxtLink
          to="/birthday"
          class="bg-pink-500 hover:bg-pink-600 text-white py-3 px-6 rounded-lg shadow text-center font-semibold transition">
          🎂 Birthday
        </NuxtLink>

        <!-- <NuxtLink
          to="/christmas"
          class="bg-green-500 hover:bg-green-600 text-white py-3 px-6 rounded-lg shadow text-center font-semibold transition">
          🎄 Christmas Card
        </NuxtLink> -->
      </div>
    </div>
  </div>
</template>
