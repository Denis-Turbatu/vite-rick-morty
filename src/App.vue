<script>
import AppCardList from './components/AppCardList.vue';
import AppSearch from './components/AppSearch.vue';
import {store} from "./store";
import axios from "axios";

export default {
  components:{
    AppCardList,
    AppSearch,
  },
  data() {
    return {
      cardArray: [],
      store,
    }
  },
  created(){
    axios.get("https://rickandmortyapi.com/api/character").then((resp) => {
      this.cardArray = resp.data.results;
      console.log(this.cardArray);
    })
  },
  methods: {
    getStatus() {
      axios.get("https://rickandmortyapi.com/api/character", {params: {status: this.store.selectedStatus}}).then((resp) => {
      this.cardArray = resp.data.results;
      console.log(this.cardArray);
    })
    }
  }
}
</script>

<template>
    <AppSearch @filter="getStatus"/>
    <AppCardList :cardArray="cardArray" />
</template>

<style lang="scss" scoped>

</style>