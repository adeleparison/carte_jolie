<template>
    <div>
        <div class="wrapper">
            <div class="info">
            <img v-bind:src="info.img" alt="Dog Unicorn"/>
            </div>
            <div class="cards">
                <div>
                    <img v-for="card in cartes.cards" :src="card"/>
                </div>
            <!--
            <ul>
                <li v-for="card in cartes.cards">
                    <img v-bind:src="cartes.cards"/>
                {{ card }}
                </li>
            </ul> -->
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            // création d'un objet
            info: {
                img : require ('../assets/chienunicorn.png'),
            },
            
            cartes: {
                cards: [require ('../assets/beige.svg'),
                        require ('../assets/orange.svg'),
                        require ('../assets/blue.svg'),
                        require ('../assets/green.svg'),
                        require ('../assets/orange-blue.svg'),
                        require ('../assets/red.svg'),
                       ]
            },
        }
    }
}
</script>

<style>
    .wrapper {
        height: 600px;
        width: 100%;
        background: #ffeff6;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    .info {
        border: 1px solid black;
        align-self: flex-end;
    }
    
    .info img {
        height: 220px;
        width: 200px;
    }
    
    .cards {
        height: 300px;
        width: 500px;
        background: blue;   
    }
    
    .cards img {
        height: 100px;
        width: 100px;
        padding: 20px;
    }
    
    /* pour faire l'animation */
    @keyframes animCards {
        0% {transform: rotate(0deg);}
        50% {transform: rotate(-10deg);}
        100% {transform: rotate(10deg);}
    }
    
    .cards img:hover {
        animation: animCards 2s linear infinite;
    }
    
</style>