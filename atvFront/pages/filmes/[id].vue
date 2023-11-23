<script setup>

    const route = useRoute();

    const {data: filme} = await useFetch(`http://localhost:8000/filmes/${route.params.id}`)



</script>

<template>
    <div>
        <h3>{{ filme.nome }}</h3>
        <p>{{ filme.descricao }}</p>
        <img :src="`http://localhost:8000/${filme.foto}`" height="300" width="250">

    </div>

</template>