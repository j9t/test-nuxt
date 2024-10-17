<template>
  <div class="container">
    <Head>
      <Title>Home</Title>
    </Head>
    <Navigation />
    <h1>Recipe Homepage</h1>
    <div class="masonry">
      <RecipeCard v-for="recipe in recipes" :key="recipe.id" :recipe="recipe" />
    </div>
  </div>
</template>

<script>
import RecipeCard from '~/components/RecipeCard.vue';
import {recipes} from '~/data/recipes.js';
import Navigation from '~/components/Navigation.vue';
import '~/pages/index.css';

export default {
  components: {
    RecipeCard,
    Navigation
  },
  data() {
    return {
      recipes
    };
  }
};
</script>