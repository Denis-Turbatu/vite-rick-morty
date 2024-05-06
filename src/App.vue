<script>
import AppCardList from './components/AppCardList.vue'
import axios from "axios";

export default {
  components:{
    AppCardList,
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
}
</script>

<template>
    <AppCardList :cardArray="cardArray" />
</template>

<style lang="scss" scoped>

</style>