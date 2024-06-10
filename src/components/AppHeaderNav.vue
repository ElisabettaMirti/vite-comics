<script>
export default {
    data(){
        return {
            NavLinks: [
                {
                    id: 1,
                    title: 'characters',
                    url: '#',
                    active: false
                },
                {
                    id: 2,
                    title: 'comics',
                    url: '#',
                    active: true
                },
                {
                    id: 3,
                    title: 'movies',
                    url: '#',
                    active: false
                },
                {
                    id: 4,
                    title: 'tv',
                    url: '#',
                    active: false
                },
                {
                    id: 5,
                    title: 'games',
                    url: '#',
                    active: false
                },
                {
                    id: 6,
                    title: 'collectibles',
                    url: '#',
                    active: false
                },
                {
                    id: 7,
                    title: 'videos',
                    url: '#',
                    active: false
                },
                {
                    id: 8,
                    title: 'fans',
                    url: '#',
                    active: false
                },
                {
                    id: 9,
                    title: 'news',
                    url: '#',
                    active: false
                },
                {
                    id: 10,
                    title: 'shop',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script>


<template>

<header>
    <section class="logo">
        <img src="../assets/img/dc-logo.png" alt="DC logo">
    </section>

    <section class="navbar">
        <nav>
            <ul>
                <li v-for="link in NavLinks" :key="link.id" :class="(link.active) ? 'active' : ''">
                    <a :href="link.url">
                        {{ link.title }}
                    </a>
                </li>
            </ul>
        </nav>
    </section>
</header>

</template>


<style lang="scss" scoped>

@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins' as *;

header{
    background-color: #ffffff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 20rem;

    ul{
        display: flex;
        

        li{
            text-transform: uppercase;
            font-weight: bolder;
            padding: 1rem;
            color: $main-black;

            &.active{
                color: $main-blue;
            }
        }
    }
}
</style>