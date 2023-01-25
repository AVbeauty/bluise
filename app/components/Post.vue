<template>
  <article>
    <blockquote>
      <p>{{ post }}</p>
    </blockquote>
  </article>
</templates>


<script>
export default {
  data: () => ({
    post: '',
  }),
  async mounted() {
    this.post = await fetch('/api/post').then((res) => res.json())
  },
}
</script>

<style scoped>
blockquote {
  border-left: 5px solid #ccc;
  padding: 0.5rem;
}
</style>
