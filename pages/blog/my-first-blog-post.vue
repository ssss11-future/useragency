<template>
  <article>
    <h1>My first blog post</h1>
    <span>Hooray!</span>
  </article>
</template>

<script>
  export default {
    async asyncData({ $content, params }) {
      const article = await $content('articles', params.slug).fetch()

      return { article }
    }
  }
</script>


