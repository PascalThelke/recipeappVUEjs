<template>
  <div>
    <Header @update-query="getRecipes" />
    <RecipeItem
      v-for="recipe in recipes"
      :key="recipe.recipe.label"
      :image="recipe.recipe.image"
      :label="recipe.recipe.label"
      :attributes="recipe.recipe.dietLabels.join(', ')"
      :url="recipe.recipe.url"
    />
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import RecipeItem from '@/components/RecipeItem.vue';

export default {
  components: {
    Header,
    RecipeItem
  },
  data() {
    return {
      recipes: [],
      currentQuery: 'sushi' // Initiale Abfrage
    }
  },
  methods: {
    async getRecipes(query) {
      // Standardwert falls query nicht gesetzt
      query = query || this.currentQuery;
      const appId = '954cd6ef';
      const appKey = 'f6d41212deced4dd72c68413b5f8014a';
      const url = `https://api.edamam.com/search?q=${query}&app_id=${appId}&app_key=${appKey}`;
      let response = await fetch(url);
      this.recipes = (await response.json()).hits;
      console.log(this.recipes);
    }
  },
  mounted() {
    this.getRecipes();
  }
}
</script>


