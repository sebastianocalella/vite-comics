<template>
    <div class="container">
        <div class="img-wrapper">
            <img :src="thumb" :alt="series + ' icon'">
        </div>
        <p>{{ series }}</p>
    </div>
</template>

<script>
export default {
    props: {
        thumb: String,
        price: String,
        series: String,
        type: String
    }
}
</script>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
    .container{
        width: calc(100%/6 - 15px);

        .img-wrapper img{
            width: 100%;
        }
    }
    p{
        color: $main-accent;
    }
</style>