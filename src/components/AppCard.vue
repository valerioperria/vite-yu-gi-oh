<script>
export default {
    props: {
        card: Object,
    },
};
</script>

<template>
    <div class="card_content" v-for="img in card.card_images">
        <img :src="img.image_url" alt="">
        <h4 class="name">{{ card.name }}</h4>
        <h4>{{ card.archetype }}</h4>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

.card_content {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: $bg-color;
    height: 100%;

    img {
        width: 100%;
        margin-bottom: 1rem;
    }

    h4 {
        text-align: center;
        max-width: 80%;
        margin-bottom: 1rem;
    }

    .name {
        color: white;
    }
}
</style>