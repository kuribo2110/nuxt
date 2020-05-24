<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        nuxt
      </h1>
      <h2 class="subtitle">
        My flawless Nuxt.js project
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
      <div class="mt-5">
        <nuxt-link :to="switchLocalePath('ja')" class="px-2">
          日本語へ
        </nuxt-link>
        <nuxt-link :to="switchLocalePath('en')" class="px-2">
          英語へ
        </nuxt-link>
        <nuxt-link :to="switchLocalePath('zh')" class="px-2">
          中国語へ
        </nuxt-link>
        <h1 class="p-3">{{ $t('lang') }}</h1>
        <nuxt-link :to="localePath('/confirm')" class="p-3">
          画面遷移
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<i18n>
  {
    "ja": {
      "lang": "日本語"
    },
    "en": {
      "lang": "English"
    },
    "zh": {
      "lang": "中文"
    }
  }
</i18n>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
