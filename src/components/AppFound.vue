<script>
import { store } from "../store";
export default {
    data() {
        return {
            store,
        };
    },
};
</script>

<template>
    <div class="nm_card">
        <p>Found {{ store.cards.length }} cards</p>
    </div>
</template>


<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

.nm_card {
    padding: 1rem;
    width: 100%;
    background-color: black;
    color: white;
}
</style>