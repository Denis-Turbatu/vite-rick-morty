<script>
import {store} from "../store";
export default {
    data(){
        return{
            store,
            status: ["Alive", "Dead", "unknown"],
        }
    }
}
</script>

<template>
    <!-- <label for="status" class="position-absolute z-1 px-1 m-5">Seleziona uno status</label> -->
    <select value="status" @change="$emit('filter')" v-model="store.selectedStatus" class="px-5 position-relative z-0 m-5">
        <option :value="state" v-for="state in status" >{{state}}</option>
    </select>
</template>

<style lang="scss">
    
</style>