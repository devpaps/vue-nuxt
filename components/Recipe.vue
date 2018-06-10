<template>

  <nuxt-link :to="'/recipes/' + id" class="asd">
    <article class="recipe">
      <div class="thumbnail">
        <picture>
          <img :src="`${thumbnail}`" alt="">
        </picture>
      </div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>

</template>


<script>
  export default {
    props: ['thumbnail', 'title', 'previewText', 'id']
  }
</script>

<style scoped>
  img {
    display: block;
    width: 100%;
    height: auto;
  }

  .asd {
      width: 400px;
  margin: 10px;
  }
</style>
