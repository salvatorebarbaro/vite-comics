<script>
 export default{
    name:"AppNavbar",
    data(){
        return{
            options:["Characters","Comics","Tv","Games","Collectibles","Videos","Fans","News","Shop"],
            // dichiarazione nulla dell'index
            // indexactive:null
            indexactive:1,
        }

        
    }
 }

</script>
<template>
    <div id="Navbar">
        <div id="container_navbar">
            <img src="/src/assets/img/dc-logo.png" alt="">
            <ul >
                            <!-- abbiamo ciclato per poter dare i valori ed il numero di valori di li    -->
                            <!-- classe dinamica in base all'index se sono uguali è active senno nulla -->
                            <!-- evento nuovo , mouse hover -->
                <li v-for="(currentoption,index) in options" :class="index == indexactive ? 'active' : '' " @mouseover="indexactive=index"> {{ currentoption }} </li>
                
            </ul>
        </div>
        
        
        
    </div>
</template>
<style lang="scss">
#Navbar{
    width: 100vw;
    background-color: white;
    color: black;
    #container_navbar{
        padding: 20px;
        display: flex;
        justify-content: center;
        gap: 480px;
        ul{
            display: flex;
            gap: 32px;
            align-items: center;
            list-style-type: none;
            li{
                font-weight:500;
                // testo in maiuscolo
                text-transform: uppercase;
                color: #464646;
                
                // comando usato per far vedere il cursore quando siamo agli li
                cursor: pointer;
                // per poter spostare il bordo sotto
                position: relative;
                // classe active
                &.active{
                    color: #0282F9;
                    &:after {
                        // elemento usato per creare il bordo fittizio da inserire
                        content: "";
                        position: absolute;
                        left: 0;
                        bottom: -40px; // Distanza dal bordo inferiore
                        // lunghezza del bordo
                        width: 100%;
                        // altezza
                        height: 3px;
                        background-color: #0282F9; // Colore del bordo inferiore
                    }
                    
                }
            }
        }
    }
    
}
</style>