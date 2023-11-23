<script setup>
    
    const { data: filmes } = await useFetch('http://localhost:8000/filmes')

</script>

<template>
    <h2>Filmes ManFlix</h2>
    <div v-for="fil in filmes">
        <h3>{{ fil.nome }}</h3>
        <div>
        <NuxtLink :to="`/filmes/${fil.id}`">
            <img :src="`http://localhost:8000/${fil.banner}`" height="200" width="250">
        </NuxtLink>
        </div>      
    </div>
</template>