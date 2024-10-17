<template>
  <div class="recipe-card">
    <img :src="recipe.image" :alt="recipe.title" />
    <h2>{{ recipe.title }}</h2>
    <p>{{ recipe.description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    recipe: {
      type: Object,
      required: true
    }
  }
};
</script>

<style scoped>
.recipe-card {
  border: 1px solid #ccc;
  padding: 20px;
  margin: 20px;
  text-align: center;
}

.recipe-card img {
  margin: auto;
  max-width: 100%;
  height: auto;
}
</style>