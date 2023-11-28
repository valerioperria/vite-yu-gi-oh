<script>
import { store } from "../store";
export default {
    data() {
        return {
            store,
        };
    },
}
</script>

<template>
    <select @change="$emit('performSelection')" v-model="store.selected">
        <option value="Ancient Gear">Ancient Gear</option>
        <option value="Alien">Alien</option>
        <option value="Ally of Justice">Ally of Justice</option>
    </select>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixins" as*;

select {
    padding: 0.5rem 2rem 0.5rem 0.5rem;
    position: absolute;
    top: 1.5%;
}
</style>
