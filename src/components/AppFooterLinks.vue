<script>
export default {
    data(){
        return {
            SocialLinks:[
                {
                    id: 1,
                    name: "Facebook",
                    logo: "./src/assets/img/footer-facebook.png"
                },
                {
                    id: 2,
                    name: "Twitter",
                    logo: "./src/assets/img/footer-twitter.png"
                },
                {
                    id: 3,
                    name: "Youtube",
                    logo: "./src/assets/img/footer-youtube.png"
                },
                {
                    id: 4,
                    name: "Pinterest",
                    logo: "./src/assets/img/footer-pinterest.png"
                },
                {
                    id: 5,
                    name: "Periscope",
                    logo: "./src/assets/img/footer-periscope.png"
                },
            ]
        }
    }
}
</script>

<template>

    <div class="footer-socials">
        <section class="sign-up-btn">
            <a href="#">sign-up now!</a>
        </section>

        <section class="links">
            <h2>follow us</h2>
            <ul>
                <li v-for="link in SocialLinks" :key="link.id">
                    <img :src="link.logo" alt="">
                </li>
            </ul>
        </section>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss';

div.footer-socials{
    position: relative;
    z-index: 1;
    background-color: #303030;
    padding: 3rem 20rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

a{
    text-transform: uppercase;
    font-weight: bolder;
    color: white;
    border: 2px solid #0282f9;
    padding: 1rem;

    &:hover{
        background-color: #5d5d5d;
    }
}

h2{
    text-transform: uppercase;
    color: $main-blue;
    margin-right: 1rem;
}

section.links,
.links>ul{
    display: flex;

    li{
        margin-right: 1rem;
    }
}

</style>