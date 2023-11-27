<script>
import { store } from "../store";
export default {
    props: {
        card: Object,
    },
}
</script>

<template>
    <select name="" id="">
        <option value="">Alien</option>
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
