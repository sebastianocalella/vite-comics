<template lang="">
    <div class="container">
        <div class="menu">
            <div class="column">
                <h2>DC COMICS</h2>
                <ul>
                    <li v-for="dcComicsItem in dcComicsItems">{{dcComicsItem.text}}</li>
                </ul>
                <h2>SHOP DC</h2>
                <ul>
                    <li v-for="shopItem in shopItems">{{shopItem.text}}</li>
                </ul>
            </div>
            <div class="column">
                <h2>DC</h2>
                <ul>
                    <li v-for="dcElement in dcList">{{dcElement.text}}</li>
                </ul>
            </div>
            <div class="column">
                <h2>SITES</h2>
                <ul>
                    <li v-for="site in sites">{{site.text}}</li>
                </ul>
            </div>
        </div>

        <div class="img-wrapper">
            <img src="../assets/images/dc-logo-bg.png" alt="dc-logo">
        </div>

        <div class="join-us-banner">
            <button>sign-up now!</button>
            <div class="social-networks">
                <h3>follow us</h3>
                <img src="../assets/images/footer-facebook.png" alt="facebook-logo">
                <img src="../assets/images/footer-twitter.png" alt="twitter-logo">
                <img src="../assets/images/footer-youtube.png" alt="youtube-logo">
                <img src="../assets/images/footer-pinterest.png" alt="pinterest-logo">
                <img src="../assets/images/footer-periscope.png" alt="periscope-logo">
            </div>
        </div>
    </div>
</template>

<script>

export default{
    data() {
        return{
            dcComicsItems: [
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
            ],
            shopItems: [
                {
                    text: "Shop DC"
                },
                {
                    text: "Shop DC Collectibles"
                }
            ],
            dcList: [
                {
                    text: "Terms Of Use"
                },
                {
                    text: "Privacy policy (New)"
                },
                {
                    text: "Ad Choices"
                },
                {
                    text: "Advertising"
                },
                {
                    text: "Jobs"
                },
                {
                    text: "Subscriptions"
                },
                {
                    text: "Talent Workshops"
                },
                {
                    text: "CPSC Certificates"
                },
                {
                    text: "Ratings"
                },
                {
                    text: "Shop Help"
                },
                {
                    text: "Contact Us"
                }
            ],
            sites: [
                {
                    text: "DC"
                },
                {
                    text: "MAD Magazine"
                },
                {
                    text: "DC Kids"
                },
                {
                    text: "DC Universe"
                },
                {
                    text: "DC Power Visa"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
    .container{
        background-image: url(../assets/images/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        display: flex;
        justify-content: space-between;
        height: calc(482px + 80px);
        padding: 0 15%;

        div.menu{
            display: flex;
            width: 42%;
            justify-content: space-between;
            padding: 25px 0;
            min-width: 450px;
            margin-top: 75px;

            h2{
                color: white;
                padding: 12px 0;
                font-size: 1.8rem;
            }
            li{
                color: $text-gray;
                padding: 1px 0;
                font-size: 1rem;

                &:hover{
                    cursor: pointer;
                    text-decoration: underline;
                    color: $text-light-gray;
                }
            }
        }
        div.img-wrapper{
                img{
                    height: 100%;
                }
            }
        .join-us-banner{
            height: 80px;
            width: 100%;
            background-color: $footer-gray-bg;
            position: fixed;
            left: 0;
            bottom: 0;
            z-index: 1;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 100px;
            min-width: 950px;

            button{
                color: $main-accent;
                text-transform: uppercase;
                background-color: transparent;
                padding: 10px;
                border: 2px solid $main-color;

                &:hover{
                    background-color: #4b4646;
                    cursor: pointer;
                }

                &:active{
                    background-color: #847676;
                    cursor: pointer;
                    border: 1px solid #448ee8;
                }
            }

            .social-networks{
                display: flex;
                align-items: center;

                h3{
                    color: $main-color;
                    text-transform: uppercase;
                    padding: 2px;
                }
                img{
                    padding: 0 8px;
                }
            }
        }
    }
</style>