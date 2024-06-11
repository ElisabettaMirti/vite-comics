<script>
export default {
    data(){
        return {
        }
    }
}
</script>

<template>
    <div class="main-content">
        <h1>
        --> Content goes here <--
        </h1>
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
        height: 10rem;
        padding: 3rem 20rem;
        color: white;
    }
</style>