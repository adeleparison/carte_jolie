<template>
    <nav>
        <h1>{{ title }}</h1>
        <p>{{ para }}</p>
    </nav>
</template>


<script>
export default {
    data() {
        return {
            title : 'DES CARTES JOLIES', 
            para: 'Envoyez une carte faite par vos soins à vos proches, pour un événement exceptionnel !',
        }
    }
}
</script>


<style scoped>
    nav {
        background: #89b6d5;
        margin: 0;
    }
    h1 {
        color: #fff;
        margin: 0;
        padding-top: 15px;
        text-align: center;
        letter-spacing: 0.05em;
    }
    
    p {
        color: #fff;
        text-align: center;
        letter-spacing: 0.03em;
        margin: 0;
        padding-top: 10px;
        padding-bottom: 15px;
        
    }
</style>