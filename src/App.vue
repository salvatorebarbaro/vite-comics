<script >
import AppNavbar from './components/AppNavbar.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppComics from './components/AppComics.vue';
export default{
    components:{
        AppNavbar,
        AppFooter,
        AppJumbotron,
        AppComics,

    },

    data(){
        return{
           
        }
    }
}
</script>

<template>
    <AppNavbar></AppNavbar>
    <AppJumbotron></AppJumbotron>
    <AppComics></AppComics>
    <AppFooter></AppFooter>
  
</template>

<style lang="scss">
@use '../src/style/generale.scss' as *;
*{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
template{
    font-family: 'Barlow Condensed', sans-serif;
}


</style>
