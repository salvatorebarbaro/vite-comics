<script>
// sezione utile a definirli 
export default{
    name:"AppSectionBlue",
    data(){
        return{
            links: [

                        {
                            title: 'Digital Comics',
                            image: '../src/assets/img/buy-comics-digital-comics.png'
                        },

                        {
                            title: 'DC Merchandise',
                            image: '../src/assets/img/buy-comics-merchandise.png'
                        },


                        {
                            title: 'Subscription',
                            image: '../src/assets/img/buy-comics-subscriptions.png'
                        },

                        {
                            title: 'Comic shop locator',
                            image: '../src/assets/img/buy-comics-shop-locator.png'
                        },

                        {
                            title: 'DC Power Visa',
                            image: '../src/assets/img/buy-dc-power-visa.svg'
                        },

                    ],
            }

        
    }
 }

</script>
<template>
    <div id="container_blue">
        <div class="container">
            <div v-for="link in links" id="section_inside">
                <img :src="link.image" :alt="link.title">
                <div id="description">{{ link.title }}</div>
                
            </div>
        </div>

    </div>

</template>
<style lang="scss">

@use '../src/style/variable.scss' as *;

#container_blue{
    background-color: $primary;
    .container{
        display:flex;
        justify-content: space-around;
        #section_inside{
            display: flex;
            align-items: center;
            gap: 18px;
            margin: 50px 0;
            cursor: pointer;
            img{
                height: 55px;
            }
            #description{
                text-transform: uppercase;
                font-size: 14px;
                font-weight: 700;
            }
        }
    }
}



</style>