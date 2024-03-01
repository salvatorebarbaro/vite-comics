<script>
// importare i componenti

import AppSectionBlue from '../components/AppSectionBlue.vue';
// sezione utile a definirli 
export default{
    name: "AppFooter",
    data() {
        return {
            linkList: [
                {
                    title: 'dc comics',
                    links: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    title: 'shop',
                    links: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    title: 'dc',
                    links: ['Terms of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    title: 'sites',
                    links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                },
            ],
            socials: [
                {
                    name: 'facebook',
                    icon: '../src/assets/img/footer-facebook.png'
                },
                {
                    name: 'twitter',
                    icon: '../src/assets/img/footer-twitter.png'
                },
                {
                    name: 'youtube',
                    icon: '../src/assets/img/footer-youtube.png'
                },
                {
                    name: 'pinterest',
                    icon: '../src/assets/img/footer-pinterest.png'
                },
                {
                    name: 'periscope',
                    icon: '../src/assets/img/footer-periscope.png'
                },
            ]
        };
    },
    components: { AppSectionBlue }
}

</script>
<template>
    <AppSectionBlue></AppSectionBlue>
    <div id="container_footer">
        <div id="container_footer_head">
            <div class="container">
                <div id="links_list">
                    <div v-for="link in linkList" id="links">
                        <h4>{{link.title}}</h4>
                        <ul>
                            <!-- ci siamo iterati all'interno di ogni sezione e a sua volta all'interno dei links per ottenete ogni link -->
                            <li v-for="currentLink in link.links">{{currentLink}}</li>
                            
                        </ul>
                    </div>
                </div>
                <div id="img">
                    <img src="/src/assets/img/dc-logo-bg.png" alt="">
                </div> 
                

            </div>

        </div>
        <div id="container_footer_Bottom">
            <div class="container" id="Container_follow">
                <button>SIGN-UP NOW!</button>
                <div id="section_social">
                    <div id="follow">follow us</div>
                    <div id="socials_link">
                        <div v-for="social in socials" id="container">
                            <img :src="social.icon" :alt="social.name">
                        </div>
                    </div>
                    
                </div>
            </div>

        </div>  

    </div>
    
</template>
<style lang="scss">

@use '../src/style/variable.scss' as *;

#container_footer{
    display: flex;
    flex-direction: column;
    #container_footer_head{
        height: 370px;
        background-image: url(../assets/img/footer-bg.jpg);
        background-repeat: no-repeat; /* Impedisce alla sfondo di ripetersi */
        background-size: cover; /* Fa sì che l'immagine si adatti all'area del contenitore senza distorcere proporzioni */
        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            overflow: hidden;
            
            #links_list{
                display: flex;
                flex-flow:column wrap;
                align-content: flex-start;
                gap: 20px 30px;
                height: 100%;
                padding: 20px 0;
            }
            h4
            {
                text-transform: uppercase;
                font-size: 1.2em;
                margin-bottom: 10px;
            }
            ul{
                list-style-type: none;
            }
            li{
                font-weight: 200;
            }
        }
    }
    #container_footer_Bottom{
        #Container_follow{
            display: flex;
            justify-content: space-between;
            align-items: center;
                button{
                    padding: 18px 15px;
                    font-weight:600 ;
                    color: white;
                    border: 2px $primary solid;
                    background-color: transparent;
                    cursor: pointer;
                    margin: 30px 0;
                }
                #section_social{
                    display: flex;
                    gap: 30px;
                    align-items: center;
                    #follow{
                        text-transform: uppercase;
                        font-size: 16px;
                        color: $primary;
                        font-weight: 700;
                    }
                    #socials_link{
                        display: flex;
                        gap: 20px;
                        align-items: center;
                        cursor: pointer;
                    }
                }
        
        
        }
        
    }

    

    
}
  

</style>