<template>
    <nav>
        <h2>{{ title }}</h2>
    </nav>
</template>


<script>
export default {
    data() {
        return {
            title : 'Cartes Jolies', 
        }
    }
}
</script>


<style scoped>
    nav {
        background: blue;
        margin: 0;
    }
    h2 {
        color: black;
        margin: 0;
    }
</style>