<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';




export default {
   data() {
     return{

     }
   },
   components: {
     AppHeader,
     AppMain,
     AppFooter
   }
}
</script>

<template>
   <AppHeader/>
   <AppMain/>
   <AppFooter/>
   

</template>

<style lang="scss">
@use 'assets/scss/main' as *;
// Import all of Bootstrap's CSS
@import "bootstrap/scss/bootstrap";

</style>
