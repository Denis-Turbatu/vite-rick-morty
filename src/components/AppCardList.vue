<script>
import AppCard from './AppCard.vue'
export default {
    components: {
        AppCard,
    }
}
</script>

<template>
    <!-- container -->
    <div class="container">
        <!-- title -->
        <h1 class="w-50 mx-auto text-center my-5">Rick and Morty App</h1>
        <!-- cards -->
        <div class="row d-flex flex-wrap col-12 gap-3 justify-content-center">
            <AppCard class="col-3"/>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>