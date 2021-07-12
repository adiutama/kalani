<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import TestimonialList from '~/data/testimonial.json'

const { t } = useI18n()
const testimonialList = TestimonialList
</script>

<template>
  <h1 id="testimonial" class="text-xl mb-4 pt-6">
    {{ t('testimonial') }}
  </h1>

  <div>
    <div v-for="(item, index) in testimonialList" :key="index" class="mt-4 first:mt-0">
      <img :src="item.path" :alt="item.label">
    </div>
  </div>
</template>
