<template>
  <header>
    <input v-model="searchQuery" @input="updateQuery" placeholder="Suche..." type="text">
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data() {
    return {
      searchQuery: ''
    }
  },
  methods: {
    updateQuery() {
      this.$emit('update-query', this.searchQuery);
    }
  }
}
</script>

<style scoped>
header {
  background-color: #f4bc39;
  height: 120px;
  display: flex;
  align-items: flex-end;
  padding: 16px;
  border-bottom-left-radius: 8px;
  border-bottom-right-radius: 8px;
}
</style>
