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
    <select @change="$emit('filter')" v-model="store.selectedStatus">
        <option :value="state" v-for="state in status" >{{state}}</option>
    </select>
</template>

<style lang="scss">
    
</style>