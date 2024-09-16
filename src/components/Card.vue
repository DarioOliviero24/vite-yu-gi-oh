<script>
   export default {
        props: {
            name: {
                type: String,
            },
            archetype: {
                type: String,
            },
            image: {
                type: String,
            }
        }
    }
</script>
<template>
    <div class="CARDcontainer">
        <div class="IMGcontainer">
            <img class="img" :src="image" alt="Card Image">
        </div>
        <div>
            <h3>{{ name }}</h3>
        </div>
        <div>
            <p>{{ archetype }}</p>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;
    .CARDcontainer {
        display: flex;
        gap: 10px;
        flex-direction: column;
        width: calc((100% / 5) - 20px);
        min-height: 300px;
        justify-items: center;
        text-align: center;
    }

    .IMGcontainer {
        width: 100%;
        height: auto;
    }

    .img {
        width: 100%;
        height: 100%;
    }
</style>