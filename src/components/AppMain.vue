<template lang="">
    <div class="black-banner">
        <h2>Content goes here</h2>
    </div>
    <div class="blue-banner">
        <ul>
            <li v-for="blueBarElement in blueBarList">
                {{blueBarElement.text}}
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
                    image: '',
                    text: 'digital comics'
                },
                {
                    image: '',
                    text: 'dc merchandise'
                },
                {
                    image: '',
                    text: 'subscription'
                },
                {
                    image: '',
                    text: 'comic shop locator'
                },
                {
                    image: '',
                    text: 'dc power visa'
                }
            ]
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
        }
    }
</style>
