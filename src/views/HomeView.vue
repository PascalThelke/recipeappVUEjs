<template>
  <RecipeItem />
  <RecipeItem />
  <RecipeItem />
  <RecipeItem />
  <RecipeItem />
</template>

<script>
import RecipeItem from '@/components/RecipeItem.vue';

export default {
  components: {
    RecipeItem
  },
  data() {
    recipes: [];
  },
  methods: {
    async getRecipes() {
      let query = 'sushi';
      const appId = '954cd6ef';
      const appKey = 'f6d41212deced4dd72c68413b5f8014a';
      const url = `https://api.edamam.com/search?q=${query}&app_id=${appId}&app_key=${appKey}`;
      let response = await fetch(url);
      this.recipes = await response.json();
      console.log(this.recipes);
    }
  },
  mounted(){
    this.getRecipes();
  }
}
</script>
