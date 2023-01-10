<template lang="">
    <div class="jumbo">
        <h3>current series</h3>
    </div>
    <div class="black-banner">
        <div class="comics-container">
            <MainComic v-for="comic in comics"
                :thumb="comic.thumb"
                :price="comic.price"
                :series="comic.series"
                :type="comic.type"/>
        </div>
        <button>load more</button>
    </div>
    <div class="blue-banner">
        <ul>
            <li v-for="blueBarElement in blueBarList">
                <img :src="getImagePath('../assets/images/'+blueBarElement.imagePath)" alt="blallo">
                <p>{{blueBarElement.text}}</p>
            </li>
        </ul>
    </div>
</template>

<script>
import MainComic from './MainComic.vue';

export default {
    components:{
        MainComic
    },
    data() {
        return {
            blueBarList: [
                {
                    imagePath: 'buy-comics-digital-comics.png',
                    text: 'digital comics'
                },
                {
                    imagePath: 'buy-comics-merchandise.png',
                    text: 'dc merchandise'
                },
                {
                    imagePath: 'buy-comics-subscriptions.png',
                    text: 'subscription'
                },
                {
                    imagePath: 'buy-comics-shop-locator.png',
                    text: 'comic shop locator'
                },
                {
                    imagePath: 'buy-dc-power-visa.svg',
                    text: 'dc power visa'
                }
            ],
            comics: [
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book"
                },
                {
                    thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel"
                }
            ]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
.jumbo{
    position: relative;
    height: 250px;
    background-image: url(../assets/images/jumbotron.jpg);
    background-size: cover;

    h3{
        position: absolute;
        color: $main-accent;
        text-transform: uppercase;
        background-color: $main-color;
        font-size: .9rem;
        padding: .6rem .8rem;
        top: calc(100% - 1rem);
        left: 12%;
    }
}
.black-banner {
    background-color: $main-dark-color;
    padding: 4rem 0;
    margin: 0 auto;

    div.comics-container{
        width: 70%;
        height: 100%;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }

    h2 {
        color: $main-accent;
        margin-left: 15%;
    }

    button{
        display: block;
        color: $main-accent;
        background-color: $main-color;
        padding: .5rem 3rem;
        text-transform: uppercase;
        border: none;
        margin: 3rem auto 0;
    }
}


.blue-banner {
    display: flex;
    align-items: center;
    height: 180px;
    background-color: $main-color;
    padding: 0 15%;

    ul {
        width: 100%;
        display: flex;
        justify-content: space-around;
    }

    li {
        color: w$main-accent;
        display: flex;
        align-items: center;
        text-transform: uppercase;

        img {
            height: 50px;
            margin-right: 10px;
        }
    }
}
</style>
