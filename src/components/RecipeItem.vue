<template>
    <div class="recipe_container">
        <img class="recipe_item_image" :src="foodImage">
        <div class="right_half">
            <div>
                {{ label }}
            </div>
            <div class="bottom_row">
                {{ attributes }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'RecipeItem',
    data() {
        return {
            foodImage: require('@/assets/logo.png'),
            label: 'Sushi-Rolls',
            attributes: 'Vegan, Fettarm '
        };
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
    align-items: center;
    gap: 8px;
    cursor: pointer;

    &:hover {
        background-color: rgba(0, 0, 0, 0.1)
    }
}

.right_half {
    display: flex;
    flex-direction: column;
    gap: 4px;
}

.bottom_row{
    color: rgba(0, 0, 0, 0.4);
    font-size: 12px;
}

.recipe_item_image {
    height: 72px;
}
</style>