<script setup>
    const { data: categorias } = await useFetch('http://localhost:8000/categoria')
</script>

<template>
    <h2>Categorias</h2> 
    <div v-for="cat in categorias">
        <span>Nome Categoria:{{ cat.nome }}</span>
    </div>
</template>