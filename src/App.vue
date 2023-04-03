<script setup>
import { ref } from 'vue'


const nome = ref('')
const email = ref('')
const senha = ref('')
const senha01 = ref('')

</script>

<template>  
<div>
  <p>Nome: </p>
<input v-model="nome" placeholder="digite seu nome"/>

<p>Email: </p>
<input v-model="email" placeholder="digete seu email"/>

<p>Senha: </p>
<input type="password" v-model="senha" placeholder="digete sua senha"/>

<p>Confirmar senha: </p>
<input type="password" v-model="senha01" placeholder="digete sua senha"/>
</div>
</template>

<style scoped>

</style>
