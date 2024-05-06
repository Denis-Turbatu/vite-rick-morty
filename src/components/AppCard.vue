<script>
export default {
    props: {
        cardObj: Object,
    },
    data() {
        return {};
    },
}
</script>

<template>
    <!-- card -->
    <div class="card ms-border-none bg-transparent">
        <!-- img -->
        <img :src="`${cardObj.image}`" class="card-img-top rounded-circle" style="width: 18rem" alt="...">
        <!-- section text -->
        <div class="card-body">
            <h2 class="card-text text-center">{{cardObj.name}}</h2>
            <p class="card-text text-center my-0">{{cardObj.status}}</p>
            <p class="card-text text-center">{{cardObj.species}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .ms-border-none{
        border: none;
    }
</style>