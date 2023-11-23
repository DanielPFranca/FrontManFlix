<script setup>
    const { data: assinatura } = await useFetch('http://localhost:8000/assinatura')
</script>

<template>
    <h2>Assinaturas ManFlix</h2>
    <div v-for="assi in assinatura">
    <span>Nome: {{ assi.nome }}</span> <br>
    <span>Valor: {{ assi.valor }}</span> <br><br>
    </div>
</template>