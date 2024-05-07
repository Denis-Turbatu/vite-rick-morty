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