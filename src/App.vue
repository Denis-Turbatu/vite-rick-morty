<script>
import AppCardList from './components/AppCardList.vue';
import AppSearch from './components/AppSearch.vue';
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
      status: ["Alive", "Dead", "unknown"]
    }
  },
  created(){
    axios.get("https://rickandmortyapi.com/api/character").then((resp) => {
      this.cardArray = resp.data.results;
      console.log(this.cardArray);
    })
  },
}
</script>

<template>
    <AppSearch />
    <AppCardList :cardArray="cardArray" />
</template>

<style lang="scss" scoped>

</style>