<script>
import axios from "axios";
import { store } from "./store";
import AppHeader from "./components/AppHeader.vue";
import CardList from "./components/CardList.vue";


export default {
  data() {
    return {
      store,
    };
  },
  created() {
    axios.get(this.store.apiUrl).then((resp) => {
      this.store.cards = resp.data.data;
    });
  },
  components: { AppHeader, CardList }
}
</script>

<template>
  <AppHeader />
  <CardList />
</template>

<style lang="scss">
@use "./style/general.scss"
</style>
