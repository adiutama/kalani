<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
</script>

<template>
  <main class="flex justify-center">
    <div class="w-full lg:w-md">
      <section class="h-full p-6">
        <header class="flex flex-col w-full items-center">
          <BrandLogo size="120px" />

          <nav class="w-full mt-6">
            <ul class="p-0">
              <li class="my-4">
                <a href="/" class="btn w-full">
                  <mdi:home /> <span class="ml-2" v-text="t('home')" />
                </a>
              </li>
              <li class="my-4">
                <a
                  href="https://wa.me/6281259538840?text=Hai+Kalani.+Mau+tanya-tanya+nih."
                  target="_blank"
                  class="btn w-full"
                >
                  <mdi:whatsapp />
                  <span class="ml-2" v-text="t('contact_us')" />
                </a>
              </li>
            </ul>
          </nav>
        </header>

        <router-view />
      </section>
    </div>
  </main>
</template>
