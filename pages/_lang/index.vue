<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        {{ $t('home.title') }}
      </h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
        <NuxtLink v-if="$i18n.locale === 'es'" :to="`/pt` + $route.fullPath" class="Header__Link" active-class="none" exact>
          {{ $t('links.portuguese') }}
        </NuxtLink>
        <NuxtLink v-else :to="$route.fullPath.replace(/^\/[^\/]+/, '')" class="Header__Link" active-class="none" exact>
          {{ $t('links.spanish') }}
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Index'
}
</script>

<style scoped>

</style>
