<script setup>
    const { data: usuarios } = await useFetch('http://localhost:8000/usuarios')
</script>

<template>
    <h2>Usuarios</h2>
    <div v-for="user in usuarios">
        <span>Nome: {{ user.nome }}</span><br>
        <span>CPF: {{ user.cpf }}</span><br>
        <span>Nascimento: {{ user.nascimento }}</span><br>
        <span>Email: {{ user.email }}</span><br>
        <span>Fone: {{ user.fone }}</span><br>
        <img :src="`http://localhost:8000/${user.foto}`" height="200" width="200"> <br><br>
    </div>
</template>