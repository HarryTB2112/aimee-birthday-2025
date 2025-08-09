<script setup lang="ts">
import { ref } from 'vue';
import type Gift from '~/lib/models/gift.interface';

definePageMeta({
  layout: 'card',
});

const showGifts = ref<boolean>(false);
const gifts = ref<Gift[]>([
  {
    name: 'Joy Crookes 🎤',
    link: 'https://www.ticketmaster.co.uk/joy-crookes-tickets/artist/2280427#about',
  },
  {
    name: 'Flowers 🌻',
  },
  {
    name: 'Find out in Leeds...',
  },
]);
</script>

<template>
  <div
    class="min-h-(--full-height-page) flex flex-col items-center justify-center bg-gradient-to-br from-purple-200 via-purple-300 to-purple-400 p-4">
    <div
      class="bg-white rounded-2xl shadow-2xl p-6 w-full max-w-lg transform transition duration-500 hover:scale-105">
      <!-- Greeting -->
      <p class="text-left text-gray-700 mb-6">Dear Aimée,</p>
      <h1 class="text-4xl font-bold text-purple-600 text-center mb-4">
        Happy Birthday! 🎂
      </h1>
      <p class="text-left text-gray-700 mb-6">
        I hope you have the best day my angel, I love you so so much!
      </p>
      <p class="text-left text-gray-700 mb-2">
        Have the best long weekend and I can't wait to go to Cape Town with you.
      </p>
      <p class="text-right text-gray-700">Lots of love,</p>
      <p class="text-right text-gray-700 mb-6">Harry xxx</p>

      <!-- Gift List Toggle -->
      <div>
        <button
          @click="showGifts = !showGifts"
          class="w-full cursor-pointer bg-purple-500 text-white py-2 rounded-lg hover:bg-purple-600 transition">
          {{ showGifts ? 'Hide' : 'Show' }} Gifts 🎁
        </button>

        <transition name="fade">
          <div v-if="showGifts" class="mt-4">
            <!-- Gifts -->
            <ul class="space-y-2">
              <li
                v-for="(gift, index) in gifts"
                :key="index"
                class="flex justify-between items-center bg-purple-50 p-2 rounded-lg">
                <a
                  v-if="gift.link"
                  class="hover:underline text-purple-500"
                  :href="gift.link"
                  target="_blank"
                  >{{ gift.name }}</a
                >
                <a v-else>{{ gift.name }}</a>
              </li>
            </ul>
          </div>
        </transition>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
