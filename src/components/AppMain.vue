<template lang="">
    <div class="black-banner">
        <h2>Content goes here</h2>
    </div>
    <div class="blue-banner">
        <ul>
            <li v-for="blueBarElement in blueBarList">
                <img :src="getImagePath('../assets/images/'+blueBarElement.image)" alt="blallo">
                <p>{{blueBarElement.text}}</p>
            </li>
        </ul>
    </div>
</template>

<script>
export default{
    data() {
        return{
            blueBarList: [
                {
                    image: 'buy-comics-digital-comics.png',
                    text: 'digital comics'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    text: 'dc merchandise'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    text: 'subscription'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    text: 'comic shop locator'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    text: 'dc power visa'
                }
            ]
        }
    },
    methods: {
        getImagePath: function(imgPath){
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<style lang="scss" scoped>
    .black-banner{
        display: flex;
        align-items: center;
        background-color: black;
        height: 160px;

        margin: 0 auto;

        h2{
            color: white;
            margin-left: 15%;
        }
    }

    .blue-banner{
        display: flex;
        align-items: center;
        height: 180px;
        background-color: #0282f9;
        padding: 0 15%;

        ul{
            width: 100%;
            display: flex;
            justify-content: space-around;
        }

        li{
            color: white;
            display: flex;
            align-items: center;
            text-transform: uppercase;

            img{
                height: 50px;
                margin-right: 10px;
            }
        }
    }
</style>
