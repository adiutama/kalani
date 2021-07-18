<script setup lang="ts">
import { useI18n } from 'vue-i18n'

const { t } = useI18n()
const showProducts = () => {
  const elmt = document.getElementById('menu')

  elmt?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <main class="flex justify-center">
    <div class="w-full lg:w-md">
      <section class="h-full">
        <header class="flex flex-col w-full h-screen items-center justify-center p-6">
          <BrandLogo size="120px" />

          <nav class="w-full mt-6">
            <ul class="p-0">
              <li class="my-4">
                <a href="/#menu" class="btn w-full" @click.prevent="showProducts">
                  <mdi:book-open-outline /> <span class="ml-2" v-text="t('menu')" />
                </a>
              </li>
              <li class="my-4">
                <a
                  href="/testimonial"
                  class="btn flex-1"
                >
                  <mdi:comment />
                  <span class="ml-2" v-text="t('testimonial')" />
                </a>
              </li>
              <li class="my-4">
                <a
                  href="https://wa.me/6281259538840?text=Hai+Kalani.+Mau+tanya-tanya+nih."
                  target="_blank"
                  class="btn flex-1"
                >
                  <mdi:whatsapp />
                  <span class="ml-2" v-text="t('contact_us')" />
                </a>
              </li>
            </ul>

            <div class="flex flex-wrap flex-row justify-center mb-4 mt-8">
              <div class="w-full mb-4 text-center">
                <span v-text="t('visit_also')" />
              </div>
              <a
                href="https://www.instagram.com/eatkalani/"
                target="_blank"
                class="btn p-2 mx-2"
              >
                <img src="/images/brand/instagram.png" alt="Instagram" class="h-6">
              </a>
              <a
                href="https://www.tokopedia.com/eatkalani/"
                target="_blank"
                class="btn p-2 mx-2"
              >
                <img src="/images/brand/tokopedia.png" alt="Tokopedia" class="h-6">
              </a>
            </div>
          </nav>
        </header>

        <div class="p-6">
          <router-view />
        </div>
      </section>
    </div>
  </main>
</template>
