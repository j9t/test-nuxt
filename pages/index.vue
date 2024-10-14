<template>
  <div>
    <h1>Recipe Homepage</h1>
    <RecipeCard v-for="recipe in recipes" :key="recipe.id" :recipe="recipe" />
  </div>
</template>

<script>
import RecipeCard from '~/components/RecipeCard.vue';

export default {
  components: {
    RecipeCard
  },
  data() {
    return {
      recipes: [
        {
          id: 1,
          title: 'Vegan Tacos',
          description: 'Delicious tacos filled with black beans, corn, and avocado.',
          image: 'https://via.placeholder.com/150'
        },
        {
          id: 2,
          title: 'Quinoa Salad',
          description: 'A refreshing salad with quinoa, cucumber, tomatoes, and a lemon vinaigrette.',
          image: 'https://via.placeholder.com/150'
        },
        {
          id: 3,
          title: 'Vegan Burger',
          description: 'A hearty burger made with a black bean patty, lettuce, and tomato.',
          image: 'https://via.placeholder.com/150'
        },
        {
          id: 4,
          title: 'Stuffed Bell Peppers',
          description: 'Bell peppers stuffed with rice, vegetables, and a tomato sauce.',
          image: 'https://via.placeholder.com/150'
        },
        {
          id: 5,
          title: 'Vegan Pancakes',
          description: 'Fluffy pancakes made with almond milk and served with maple syrup.',
          image: 'https://via.placeholder.com/150'
        }
      ]
    };
  }
};
</script>

<style scoped>
h1 {
  text-align: center;
  margin-bottom: 20px;
}
</style>