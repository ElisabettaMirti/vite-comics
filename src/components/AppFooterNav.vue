<script>
export default {
    data(){
        return {
            DcComicsLinks:[
                {
                    id: 1,
                    name: 'Characters',
                },
                {
                    id: 2,
                    name: 'Comics',
                },
                {
                    id: 3,
                    name: 'Movies',
                },
                {
                    id: 4,
                    name: 'TV',
                },
                {
                    id: 5,
                    name: 'Games',
                },
                {
                    id: 6,
                    name: 'Collectibles',
                },
                {
                    id: 7,
                    name: 'Videos',
                },
                {
                    id: 8,
                    name: 'Fans',
                },
                {
                    id: 9,
                    name: 'News',
                },
                
            ],
            ShopLinks:[
                {
                    id: 1,
                    name: 'Shop DC',
                },
                {
                    id: 2,
                    name: 'Shop DC Collectibles',
                },
            ],
            DcLinks:[
                {
                    id: 1,
                    name: 'Terms Of Use',
                },
                {
                    id: 2,
                    name: 'Privacy policy (new)',
                },
                {
                    id: 3,
                    name: 'Ad Choices',
                },
                {
                    id: 4,
                    name: 'Advertiosing',
                },
                {
                    id: 5,
                    name: 'Jobs',
                },
                {
                    id: 6,
                    name: 'Subscriptions',
                },
                {
                    id: 7,
                    name: 'Talent Workshops',
                },
                {
                    id: 8,
                    name: 'CPS Certificates',
                },
                {
                    id: 9,
                    name: 'Ratings',
                },
                {
                    id: 10,
                    name: 'Shop help',
                },
                {
                    id: 11,
                    name: 'Contact Us',
                },
            ],
            SitesLinks:[
                {
                    id: 1,
                    name: 'DC',
                },
                {
                    id: 2,
                    name: 'Mag Magazine',
                },
                {
                    id: 3,
                    name: 'DC Kids',
                },
                {
                    id: 4,
                    name: 'DC Universe',
                },
                {
                    id: 5,
                    name: 'DC Power Visa',
                },
            ],
        }
    }
}
</script>

<template>
    <div class="footer-container">
        <section class="navbar">
            <nav>
                <section class="nav-one">
                    <h3>dc comics</h3>
                    <ul>
                        <li v-for="link in DcComicsLinks" :key="link.id">
                            {{ link.name }}
                        </li>
                    </ul>

                    <h3>shop</h3>
                    <ul>
                        <li v-for="link in ShopLinks" :key="link.id">
                            {{ link.name }}
                        </li>
                    </ul>
                </section>
                <section class="nav-two">
                    <h3>dc</h3>
                    <ul>
                        <li v-for="link in DcLinks" :key="link.id">
                            {{ link.name }}
                        </li>
                    </ul>
                </section>
                <section class="nav-three">
                    <h3>sites</h3>
                    <ul>
                        <li v-for="link in SitesLinks" :key="link.id">
                            {{ link.name }}
                        </li>
                    </ul>
                </section>
            </nav>
        </section>

        <section class="dc-logo">
            <img src="../assets/img/dc-logo-bg.png" alt="DC main logo">
        </section>
    </div>
    
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss';

    div.footer-container{
        padding: 0 20rem;
        display: flex;
        justify-content: space-between;
        background-image: url(../assets/img/footer-bg.jpg);
    }

    section.navbar{
            padding: 2rem 1rem;

            nav{
                display: flex;

                h3{
                    color: white;
                    text-transform: uppercase;
                    margin: 1rem 0;
                }
            }
        }

    ul>li{
        color: #707070;
        padding: .2rem;

        &:hover{
            text-decoration: underline;
            cursor: pointer;
        }
    }

    .nav-one,
    .nav-two,
    .nav.three{
        margin-right: 2rem;
    }

section.dc-logo{
    position: relative;

    img{
        position: absolute;
        right: 50%;
        bottom: -10%;
    }
}

</style>