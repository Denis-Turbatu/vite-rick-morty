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
    <div class="card">
        <!-- img -->
        <img src="..." class="card-img-top" alt="...">
        <!-- section text -->
        <div class="card-body">
            <p class="card-text">{{cardObj.name}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>