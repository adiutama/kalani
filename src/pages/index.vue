<script setup lang="ts">
import { useI18n } from 'vue-i18n'
import MenuList from '~/data/menu.json'

const { t } = useI18n()
const menu = MenuList
</script>

<template>
  <div class="h-full p-6">
    <header class="flex flex-col items-center">
      <BrandLogo size="120px" />

      <nav>
        <ul>
          <li>
            <a href="#menu" class="btn w-full">
              <mdi:book-open-outline /> <span class="ml-2" v-text="t('menu')" />
            </a>
          </li>
          <li>
            <a
              href="https://wa.me/6281259538840?text=Hai+Kalani.+Mau+tanya-tanya+nih."
              target="_blank"
              class="btn w-full"
            >
              <mdi:whatsapp /> <span class="ml-2" v-text="t('contact_us')" />
            </a>
          </li>
          <li>
            <a
              href="https://www.instagram.com/eatkalani/"
              target="_blank"
              class="btn w-full"
            >
              <mdi:instagram /> <span class="ml-2" v-text="'Instagram'" />
            </a>
          </li>
          <li>
            <a
              href="https://www.instagram.com/stories/highlights/17878482257404263/"
              target="_blank"
              class="btn w-full"
            >
              <mdi:comment /><span class="ml-2" v-text="t('testimonial')" />
            </a>
          </li>
        </ul>
      </nav>
    </header>

    <div id="menu" class="mt-10">
      <h2 class="text-xl mb-4">
        {{ t('menu') }}
      </h2>

      <div>
        <Card
          v-for="(item, index) in menu"
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
              <mdi:whatsapp /> <span
                class="ml-2"
                v-text="t('order')"
              />
            </a>
          </template>
        </Card>
      </div>
    </div>
  </div>
</template>

<style scoped>
header {
  @apply w-full;
}

nav {
  @apply w-full mt-6;
}

nav ul {
  @apply m-0 p-0;
}

ul li + li {
  @apply mt-4;
}
</style>
