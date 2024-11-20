<template>
    <a :href="url" class="recipeContainer">
        <img class="recipe-image" :src="image">
        <div>
            <h4>Name:</h4>
            {{ label }}
        </div>
        <div>
            <h4>Source:</h4>
            {{ source }}
        </div>
    </a>
</template>

<script>

export default {
    name: 'RecipeItem',
    props: {
        image: String,
        label: String,
        source: String,
        url: String
    },
    methods: {
        goToRecept() {

        }
    }

}
</script>

<style scoped>
.recipeContainer {
    border: 1px solid rgba(0, 0, 0, 0.2);
    padding: 8px;
    border-radius: 8px;
    margin: 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-decoration: none;
    color: black;
    text-align: center;
}

.recipeContainer:hover {
    background-color: rgba(0, 0, 0, 0.2);
    ;

}

.recipe-image {
    height: 60px;
    border-radius: 8px;
}
</style>