<template>
    <nav>
        <h2>{{ title }}</h2>
    </nav>
</template>


<script>
export default {
    data() {
        return {
            title : 'DES CARTES JOLIES', 
        }
    }
}
</script>


<style scoped>
    nav {
        background: #89b6d5;
        margin: 0;
    }
    h2 {
        color: #fff;
        margin: 0;
        padding: 20px;
        text-align: center;
        letter-spacing: 0.05em;
    }
</style>