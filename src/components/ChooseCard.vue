<template>
    <div>
        <div class="wrapper">
            <div class="info">
            <!-- v-if = affiche si -->
            <img v-bind:src="info.img" alt="Dog Unicorn" v-if="!select"/>
            <img v-bind:src="info.img2" alt="Dog Unicorn" v-if="select"/>
            </div>
            <!-- v-if="select == false" -->
            <div class="cards" v-if="!select">
                <div>
                    <img v-for="card in cartes.cards" :src="card" @click="changeImg"/>
                </div>
            </div>
            <div class="custom" v-if="select">
                <app-CustomCard></app-CustomCard>
            </div>
        </div>
    </div>
</template>

<script>
// importation du fichier CustomCard
import CustomCard from './CustomCard.vue'
export default {
    components: {
        'app-CustomCard' : CustomCard,
    },
    // data = que pour les variables
    data() {
        return {
            // création d'un objet = ,
            info: {
                img : require ('../assets/dog_bul_1.png'),
                img2 : require ('../assets/dog_bul_2.png')
            },
            
            cartes: {
                cards: [require ('../assets/beige_bul.svg'),
                        require ('../assets/orange_bul.svg'),
                        require ('../assets/blue_svg.svg'),
                        require ('../assets/green_bul.svg'),
                        require ('../assets/red_bul.svg'),
                        require ('../assets/orange-blue_bul.svg'),
                       ]
            },
            
            select: false,
        }
    },
    // methods = que pour les méthodes
    methods: {
        //création d'un function = ;
        changeImg: function() {
            this.select = true; 
        }
    }
    
}
</script>

<style>
    .wrapper {
        height: 552px;
        width: 100%;
        background: #e5f4ff;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    .info {
        /*border: 1px solid black;*/
        align-self: flex-end;
        height: 400px;
        width: 430px;
        padding-bottom: 20px;
    }
    
    .info img {
        height: 400px;
        width: 430px;
    }
    
    .cards {
        height: 350px;
        width: 600px;
        /*border: 1px solid black;*/  
    }
    
    .cards img {
        height: 150px;
        width: 180px;
        padding-left: 15px;
        padding-top: 15px;
        /*changer la personnalité de la souris*/
        cursor: pointer;

    }
    
    /* pour faire l'animation */
    @keyframes animCards {
        0% {transform: rotate(-5deg);}
        12.5% {transform: rotate(0deg);}
        25% {transform: rotate(5deg);}
        50% {transform: rotate(10deg);}
        62.5% {transform: rotate(5deg);}
        75% {transform: rotate(0deg);}
        100% {transform: rotate(-5deg);}
    }
    
    .cards img:hover {
        animation: animCards 2s linear infinite;
    }
    
</style>