<script>
export default {
    data(){
        return {
            
        }
    }
}
</script>

<template>

<section class="jumbo"></section>

</template>

<style lang="scss" scoped>
@use '../styles/general.scss';
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins' as *;

section.jumbo{
    height: 400px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
}

</style>