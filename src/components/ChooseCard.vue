<template>
    <div>
        <div class="wrapper">
            <div class="info">
            <img v-bind:src="info.img" alt="Dog Unicorn"/>
            </div>
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
                img : require ('../assets/chienunicorn.png'),
            },
            
            cartes: {
                cards: [require ('../assets/beige.svg'),
                        require ('../assets/orange.svg'),
                        require ('../assets/blue.svg'),
                        require ('../assets/green.svg'),
                        require ('../assets/red.svg'),
                        require ('../assets/orange-blue.svg'),
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
        height: 560px;
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
    }
    
    .info img {
        height: 400px;
        width: 430px;
    }
    
    .cards {
        height: 350px;
        width: 600px;
        border: 1px solid black;  
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