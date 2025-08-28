<template>
  <div
    class="bg-white rounded-xl shadow-md p-6 flex flex-col justify-between border border-gray-300 hover:shadow-lg transition"
  >
    <div class="flex items-center space-x-3 mb-3" v-if="icon || title">
      <div v-if="icon" class="bg-azul text-white p-3 rounded-lg text-xl">
        <FontAwesomeIcon :icon="icon" />
      </div>
      <h3 v-if="title" class="text-lg text-vermelho font-semibold">{{ title }}</h3>
    </div>
    <p v-if="description" class="text-gray-600 flex-1 mb-4">
      {{ description }}
    </p>
    <slot />
  </div>
</template>

<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

defineProps({
  title: String,
  description: String,
  icon: [String, Array, Object]
})
</script>