<template>
  <section class="section">
    <div class="container is-max-desktop">
      <Article v-for="article in articles" :key="article.id" v-bind="article" />
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    return {
      articles: await $axios.$get('http://localhost:3301/articles')
    }
  }
}
</script>
