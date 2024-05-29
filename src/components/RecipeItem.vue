<template>
    <a :href="url" class="recipe_container">
        <img class="recipe_item_image" :src="image">
        <div class="right_half">
            <div>
                {{ label }}
            </div>
            <div class="bottom_row">
                {{ attributes }}
            </div>
        </div>
    </a>
</template>

<script>

export default {
    name: 'RecipeItem',
    props: {
        image: String,
        label: String,
        attributes: String,
        url: String,
    }
}

</script>

<style scoped>
.recipe_container {
    border: 1px solid rgba(0, 0, 0, 0.2);
    padding: 8px;
    margin: 8px;
    border-radius: 8px;
    display: flex;
    /* align-items: center; */
    gap: 8px;
    cursor: pointer;
    font-size: 22px;
    text-decoration: none;
    color: rgba(0, 0, 0, 0.9);
    &:hover {
        background-color: rgba(0, 0, 0, 0.1)
    }
}

.right_half {
    display: flex;
    flex-direction: column;
    gap: 2px;
}

.bottom_row{
    color: rgba(0, 0, 0, 0.4);
    font-size: 12px;
}

.recipe_item_image {
    height: 72px;
    border-radius: 8px;
}
</style>