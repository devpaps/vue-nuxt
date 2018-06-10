<template>
  <section class="single-recipe">
    <h1>{{ $route.params.id }}</h1>
    <div>
      <img src="" alt="">
    </div>
    <p>Description</p>
  </section>
</template>


<style scoped>
  .single-recipe {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-direction: column;
  }
</style>
