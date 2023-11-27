<script>
import { store } from "../store";
import AppCard from "./AppCard.vue"
import AppFound from "./AppFound.vue";
import AppSelect from "./AppSelect.vue";

export default {
    data() {
        return {
            store,
        };
    },
    components: { AppCard, AppFound, AppSelect },
}
</script>

<template>
    <div class="container">
        <AppSelect />
        <div class="small_container">
            <AppFound />
            <div class="wrapper">
                <div class="card" v-for="(card) in store.cards">
                    <AppCard :card="card" />
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

.container {
    padding: 5rem;
    background-color: $bg-color;
    position: relative;

    .small_container {
        padding: 2rem;
        background-color: white;

        .wrapper {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            width: 100%;
            gap: 1rem;
            background-color: white;

            .card {
                width: calc(20% - 1rem);
            }
        }
    }
}
</style>