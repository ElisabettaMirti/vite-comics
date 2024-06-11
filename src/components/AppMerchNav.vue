<script>
export default {
    data(){
        return {
            MerchLinks: [
                {
                id: 1,
                name: "digital comics",
                logo: "buy-comics-digital-comics.png"
                },
                {
                id: 2,
                name: "dc merchandise",
                logo: "buy-comics-merchandise.png"
                },
                {
                id: 3,
                name: "subscription",
                logo: "buy-comics-subscriptions.png"
                },
                {
                id: 4,
                name: "comic shop locator",
                logo: "buy-comics-shop-locator.png"
                },
                {
                id: 5,
                name: "dc power visa",
                logo: "buy-dc-power-visa.svg"
                },
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

<template>

<section class="merch-nav">
    <ul>
        <li v-for="item in MerchLinks" :key="item.id">
            <img :src="getImagePath(`../assets/img/${item.logo}`)" :alt="item.name">
            <span>{{ item.name.toUpperCase() }}</span>
        </li>
    </ul>
</section>

</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins' as *;

section.merch-nav{
    background-color: $main-blue;
    padding: 0 20rem;

    ul{
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 4rem 2rem;

        li{
            display: flex;
            align-items: center;
        }

        li>span{
            color: white;
            margin-right: 2rem;
        }

        li>img{
            height: 4rem;
            max-width: 4rem;
            margin-right: 1rem;
        }
    }
}
</style>