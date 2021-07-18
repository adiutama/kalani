<script setup lang="ts">
const props = defineProps({
  name: String,
  price: String,
  cover: String,
  description: String,
})

const name = props.name
const price = props.price
const cover = props.cover
const description = props.description
</script>

<template>
  <section class="shadow rounded overflow-hidden">
    <div>
      <img :src="cover" :alt="name">
    </div>
    <div class="p-4">
      <h1 class="text-lg font-bold" v-text="name" />
      <p v-text="price" />

      <p class="mt-2 mb-4" v-text="description" />

      <div class="flex flex-row justify-end">
        <slot name="actions" />
      </div>
    </div>
  </section>
</template>
