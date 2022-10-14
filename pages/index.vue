<template>
  <div class="main">
    <cv-settings id="settings" class="settings"></cv-settings>
    <cv-preview></cv-preview>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import CvSettings from '../components/CvSettings.vue';
import CvPreview from '../components/CvPreview.vue';

const CVFY_IMAGE = 'https://cvfy.xyz/CvFy-no-border.png';

export default Vue.extend({
  name: 'Index',
  components: { CvSettings, CvPreview },
  head() {
    return {
      title: 'Resuminator',
      link: [
        {
          rel: 'preload',
          as: 'image',
          href: 'https://cdn.ko-fi.com/cdn/kofi5.png?v=3',
        },
      ],
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'With Resuminator you can create, preview and save your CV as PDF easily and for free! Built with Nuxt.',
        },
        {
          hid: 'author',
          name: 'author',
          content: 'Mrudul Kolambe',
        },
        {
          hid: 'og:image',
          property: 'og:image',
          content: CVFY_IMAGE,
        },
        {
          hid: 'og:author',
          property: 'og:author',
          content: 'Mrudul Kolambe',
        },
        {
          hid: 'og:title',
          property: 'og:title',
          content: 'Resuminator',
        },
        {
          hid: 'og:description',
          property: 'og:description',
          content: 'With Resuminator you can create, preview and save your CV as PDF easily and for free! Built with Nuxt.',
        },
      ],
    };
  },
});
</script>
<style lang="postcss" scoped>
@media screen and (min-width: 1024px) {
  .main {
    @apply flex h-full;
  }
  .settings {
    @apply overflow-y-auto w-5/12;
  }
}
</style>
