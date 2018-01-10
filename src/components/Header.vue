<template>
    <nav>
        <h2>{{ title }}</h2>
    </nav>
</template>


<script>
export default {
    data() {
        return {
            title : 'CARTES JOLIES', 
        }
    }
}
</script>


<style scoped>
    nav {
        background: #cc3876;
        margin: 0;
    }
    h2 {
        color: #fff;
        margin: 0;
        padding: 20px;
        text-align: center;
    }
</style>