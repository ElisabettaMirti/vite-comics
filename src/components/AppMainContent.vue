<script>
import LatestComicsList from './LatestComicsList.vue';

export default {
    data(){
        return {
            
        }
    },
    components: {
        LatestComicsList
    }
}
</script>

<template>
    <div class="main-content">
        <LatestComicsList/>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins' as *;

    div.main-content{
        position: relative;
        z-index: 1;
        display: flex;
        align-items: center;
        background-color: $main-black;
        padding: 3rem 20rem 1.8rem;
        color: white;
    }
</style>