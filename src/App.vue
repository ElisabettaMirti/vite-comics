<script>
import AppHeaderNav from './components/AppHeaderNav.vue';
import AppMainContent from './components/AppMainContent.vue';
import AppMerchNav from './components/AppMerchNav.vue';
import AppFooterNav from './components/AppFooterNav.vue';
import AppFooterLinks from './components/AppFooterLinks.vue';

export default {
  data(){

  },
  components: {
    AppHeaderNav,
    AppMainContent,
    AppMerchNav,
    AppFooterNav,
    AppFooterLinks
  }
}
</script>

<template>
  <AppHeaderNav/>

  <main>
    <AppMainContent/>
    <AppMerchNav/>
  </main>
  

  <footer>
    <AppFooterNav/>
    <AppFooterLinks/>
  </footer>
  
</template>

<style lang="scss" scoped>
  @use './styles/partials/mixins.scss' as *;
  @use './styles/partials/variables.scss' as *;
  @use './styles/general.scss';

</style>
