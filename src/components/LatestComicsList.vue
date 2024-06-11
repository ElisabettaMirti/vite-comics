<script>
export default {
    data(){
        return {
            CurrentSeriesList: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ]
        }
    }
}
</script>

<template>

<div class="container">
    <div class="current-titles">
        <h2>current series</h2>
    </div>
    <section class="latest-comics">
    <article v-for="(article, index) in CurrentSeriesList" :key="index">
        <div class="img-cover">
            <img :src="article.thumb" :alt="article.series">
        </div>        
        <h4>{{ article.series.toUpperCase() }}</h4>
    </article>
    </section>
    <div class="button">
        <p>load more</p>
    </div>
</div>



</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins' as *;

div.container{
    position: relative;

    div.current-titles{
        background-color: $main-blue;
        width: 250px;
        position: absolute;
        top: -75px;
        left: -22px;

        h2{
            text-transform: uppercase;
            text-align: center;
            padding: .7rem 1rem;
        }
    }
}

section{
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-content: center;
    flex-wrap: wrap;
    padding-top: 1rem;

    article{
        width: calc((100%/6) - 1rem);
        margin-bottom: 3rem;
        align-self: flex-start;

        img{
            width: 260px;
            height: 260px;
            object-fit: cover;
            object-position: top;
            margin-bottom: 1rem;
        }
    }
}

div.button{
    display: flex;
    justify-content: center;
    align-items: center;

    p{
        text-transform: uppercase;
        background-color: $main-blue;
        color: white;
        padding: .8rem 5rem;
        font-weight: bolder;
        cursor: pointer;

        &:hover{
            background-color: #57a8f5;
        }
    }
}
</style>