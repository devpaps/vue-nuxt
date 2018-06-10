<template>
  <section class="container">
    <h1 class="title">Vue.js NuXT Recipes</h1>
    <section class="recipes">

      <Recipe
        v-for="recipe in recipes" :key="recipe.id"
        :thumbnail="recipe.thumbnail"
        :title="recipe.title"
        :id="recipe.id"
        :previewText="recipe.previewText" />

    </section>
  </section>
</template>

<script>
import Recipe from '@/components/Recipe';
  export default {
    components: {
      Recipe
    },
    asyncData() {
      return new Promise((resolve, reject) =>
      setTimeout(() => {
        resolve({
          recipes: [
            {
              id: '1',
              title: 'Totally perfect hamburger!',
              previewText: 'Awesome and sweet!',
              thumbnail: 'https://imagesvc.timeincapp.com/v3/mm/image?url=https%3A%2F%2Fcdn-image.foodandwine.com%2Fsites%2Fdefault%2Ffiles%2Fstyles%2Fmedium_2x%2Fpublic%2F1519844002%2Ffast-food-mobile-apps-chick-fil-a-FT-BLOG0218.jpg%3Fitok%3D7d_gu0JA&w=800&q=85'
            },
            {
              id: '2',
              title: 'Wrapper',
              previewText: 'This is an awesome wrapper i tasted yesterday',
              thumbnail: 'https://food.fnr.sndimg.com/content/dam/images/food/fullset/2018/6/0/FN_snapchat_coachella_wingman%20.jpeg.rend.hgtvcom.616.462.suffix/1523633513292.jpeg'

            }
          ]
        })
      }, 1500)
      )
    }
  };
</script>

<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
  margin-bottom: 2rem;
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

.recipes {
  display: flex;
  flex-flow: row wrap;
}

</style>
