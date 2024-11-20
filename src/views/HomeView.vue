<template>
  <RecipeItem :image="recipe.recipe.image" :label="recipe.recipe.label" :source="recipe.recipe.source"
    :url="recipe.recipe.url" v-for="(recipe, index) in recipes" :key="index" :recipe="recipe" />
</template>

<script>
import RecipeItem from '@/components/RecipeItem.vue';
export default {
  components: {
    RecipeItem
  },
  data() {
    return {
      recipes: []

    }
  },
  methods: {
    async getrecipes() {
      const query = 'curry';
      const appId = '18ceb50c';
      const appKey = 'bb2f21826a4f1334e101d2dfa29e4c57'
      const url = `https://www.edamam.com/search?q=${query}&app_id=${appId}&app_key=${appKey}`
      let res = await fetch(url);
      this.recipes = (await res.json()).hits;
      console.log(this.recipes);

    }
  },
  mounted() {
    this.getrecipes();
  }
}
</script>
