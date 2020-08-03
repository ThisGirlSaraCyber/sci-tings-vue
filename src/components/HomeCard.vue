<template>  
    <b-card :header="header" :title ="title" header-class="hclass">
        <b-card-text><slot></slot></b-card-text>
    </b-card>
</template>

<script>
export default {

    props:["header","title"]
}
</script>

<style scoped>
    .hclass{
        color:#28a745;
        font-weight:bold;
    }
</style>