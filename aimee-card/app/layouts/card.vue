<template>
  <div class="flex flex-col">
    <!-- Top Bar -->
    <header class="bg-white shadow-md">
      <div class="max-w-4xl mx-auto flex items-center p-4">
        <NuxtLink
          to="/"
          class="bg-purple-500 text-white px-4 py-2 rounded-lg shadow hover:bg-purple-600 transition font-semibold">
          ⬅ Home
        </NuxtLink>
      </div>
    </header>

    <!-- Page Content -->
    <main class="flex-1">
      <slot />
    </main>
  </div>
</template>
