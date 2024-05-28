<template>
    <header>
        <input placeholder="Suche..." type="text">
    </header>
 
</template>

<script>
    export default {
        name: 'header',
    }
</script>

<style scoped>
Header {
    background-color: #f4bc39;
    height: 120px;
    display: flex;
    align-items: flex-end;
    padding: 16px;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
}
</style>