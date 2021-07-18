<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <h1 id="testimonial" class="text-xl mb-4 pt-6">
    {{ t('testimonial') }}
  </h1>

  <div>
    <img src="/images/testimonial/testimonial-001.jpeg" alt="Testimonial 1">
    <img src="/images/testimonial/testimonial-002.jpeg" alt="Testimonial 2">
    <img src="/images/testimonial/testimonial-003.jpeg" alt="Testimonial 3">
    <img src="/images/testimonial/testimonial-004.jpeg" alt="Testimonial 4">
  </div>
</template>
