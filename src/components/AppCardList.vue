<script>
import AppCard from './AppCard.vue'
export default {
    components: {
        AppCard,
    },
    props: {
        cardArray: Array,
    },
    data() {
        return {};
    },
}
</script>

<template>
    <!-- container -->
    <div class="container">
        <!-- title -->
        <h1 class="w-50 mx-auto text-center my-5">Rick and Morty App</h1>
        <!-- cards -->
        <div class="row gap-3 justify-content-center">
            <div class="col" v-for="card in cardArray">
                <AppCard :cardObj="card"/>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>