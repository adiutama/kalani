<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import ProductList from '~/data/products.json'

const { t } = useI18n()
const products = ProductList
</script>

<template>
  <h1 id="menu" class="text-xl mb-4 pt-6">
    {{ t('menu') }}
  </h1>

  <div>
    <Card
      v-for="(item, index) in products"
      :key="index"
      v-bind="item"
      class="mb-4"
    >
      <template #actions>
        <a
          :href="`https://wa.me/6281259538840?text=Hai+Kalani.+Mau+pesan+${ item.name.replace(' ', '+') }.`"
          target="_blank"
          class="btn"
        >
          <mdi:whatsapp />
          <span
            class="ml-2"
            v-text="t('order')"
          />
        </a>
      </template>
    </Card>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
