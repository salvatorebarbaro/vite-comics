<script>
// sezione utile a definirli 
export default{
    name:"AppJumbotron",
    data(){
        return{
            
            }

        
    }
 }

</script>
<template>

<div id="container_jumbotron">
    <div class="container">
        <h2>Current Series</h2>
    </div>
    
</div>

  
</template>
<style lang="scss">
@use '../src/style/variable.scss' as *;

#container_jumbotron{
    height: 350px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    .container{
        position: relative;
        height: 100%;
        


        h2{
        text-transform: uppercase;
        position: absolute;
        bottom: -25px;
        left: 0;
        padding: 6px 24px;
        background-color: $primary;
    }
    }
    


    
}



</style>