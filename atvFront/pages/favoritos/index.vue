<script setup>
    const { data: favoritos } = await useFetch('http://localhost:8000/favoritos')
</script>

<template>
    <h2>Favoritos</h2>
    <div v-for="fav in favoritos">
        <span>Usuario: {{ fav.idUsuarioFK.nome }}</span><br>
        <span>Filme: {{ fav.idFilmeFK.nome }}</span>
    </div>
    
</template>