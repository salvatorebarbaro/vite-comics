<script >
import AppNavbar from './components/AppNavbar.vue';
import AppFooter from './components/AppFooter.vue';
export default{
    components:{
        AppNavbar,
        AppFooter,
    },

    data(){
        return{
           
        }
    }
}
</script>

<template>
    <AppNavbar></AppNavbar>
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
