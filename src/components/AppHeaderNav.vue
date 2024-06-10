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
                    active: false
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
                <li v-for="link in NavLinks" :key="link.id">
                    {{ link.title }}
                </li>
            </ul>
        </nav>
    </section>
</header>

</template>


<style lang="scss" scoped>

header{
    background-color: #ffffff;
}
</style>