<template lang="">
    <div class="container">
        <img src="../assets/images/dc-logo.png" alt="ciao">
        <nav>
            <ul>
                <li v-for="navBarItem in navBarItems">{{navBarItem.text}}</li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default{
    data() {
        return{
            navBarItems: [
                {
                    text: "characters"
                },
                {
                    text: "comics"
                },
                {
                    text: "movies"
                },
                {
                    text: "tv"
                },
                {
                    text: "games"
                },
                {
                    text: "collectibles"
                },
                {
                    text: "videos"
                },
                {
                    text: "fans"
                },
                {
                    text: "news"
                },
                {
                    text: "shop"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .container{
        display: flex;
        width: 70%;
        margin: 0 auto;
        padding: 30px 0;
        justify-content: space-between;

        ul{
            display: flex;
            list-style-type: none;
            height: 100%;

            li{
                padding: 0 .4rem;
                height: 100%;
                line-height: 6rem;
            }
        }
    }
</style>