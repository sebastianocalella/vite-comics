<template>
    <div class="container">
        <div class="blanket"></div>
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
        width: calc(100%/6);
        padding: 10px 10px 20px;
        position: relative;

        .blanket{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: white;
            opacity: 0;
            transition: .8s;
        }

        &:hover {
            cursor: pointer;
            .blanket{
                opacity: .2;
            }
        }
        .img-wrapper img{
            width: 100%;
            position: relative;
            z-index: 1;
        }
    }
    p{
        color: $main-accent;
        text-transform: uppercase;
        font-size: .7rem;
        margin-top: 12px;
    }
</style>