<template lang="">
    <div class="container">
        <img src="../assets/images/dc-logo.png" alt="ciao">
        <nav>
            <ul>
                <li v-for="navBarItem in navBarItems" :class="navBarItem.active ? 'active' : ''">{{navBarItem.text}}</li>
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
                    text: "characters",
                    active: false
                },
                {
                    text: "comics",
                    active: true
                },
                {
                    text: "movies",
                    active: false
                },
                {
                    text: "tv",
                    active: false
                },
                {
                    text: "games",
                    active: false
                },
                {
                    text: "collectibles",
                    active: false
                },
                {
                    text: "videos",
                    active: false
                },
                {
                    text: "fans",
                    active: false
                },
                {
                    text: "news",
                    active: false
                },
                {
                    text: "shop",
                    active: false
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

    @use '../styles/partials/variables' as *;
    .container{
        display: flex;
        width: 70%;
        margin: 0 auto;
        justify-content: space-between;

        img{
            margin: 15px 0;
        }

        ul{
            display: flex;
            height: 100%;

            li{
                padding: 0 .5rem;
                height: 100%;
                line-height: 8rem;
                text-transform: uppercase;
                font-size: .8rem;
                font-weight: 700;
            }

            li.active{
                color: $main-color;
                border-bottom: 3px solid $main-color;
            }
        }
    }
</style>