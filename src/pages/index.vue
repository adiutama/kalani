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
          class="btn w-full mr-1"
        >
          <img src="/images/brand/whatsapp.png" class="h-4" />
          <span
            class="ml-2"
          >
            Whatsapp
          </span>
        </a>
        <a
          :href="item.links.tokopedia"
          target="_blank"
          class="btn w-full ml-1"
        >
          <img src="/images/brand/tokopedia.png" class="h-4" />
          <span
            class="ml-2"
          >
            Tokopedia
          </span>
        </a>
      </template>
    </Card>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
