<script setup>
import { ref } from 'vue'


const nome = ref('')
const email = ref('')
const senha = ref('')
const senha01 = ref('')
const data = ref('')
const endereco = ref('')
const cidade = ref('')
const estado = ref('')
const hobbies = ref('')
const linguagemp = ref('')
const biografia = ref('')
</script>

<template>  
  <form action="">
    
<div class="estrutura">
  <p>Nome: </p>
<input type="text" v-model="nome" placeholder="digite seu nome"/>

<p>Email: </p>
<input type="email" v-model="email" placeholder="digete seu email"/>

<p>Senha: </p>
<input type="password" v-model="senha" placeholder="digete sua senha"/>

<p>Confirmar senha: </p>
<input type="password" v-model="senha01" placeholder="digete sua senha"/>
<div >senha correta</div>
<div >senha incorreta</div>

<p>data de nacimento:</p>
<input type="date" v-model="data">

<p>endereço:</p>
<input type="text" v-model="endereco" placeholder="rua; N° da casa"/>

<p>cidade:</p>
<input type="string" v-model="cidade" placeholder="digite sua cidade"/>

<p>estado:</p>

<select v-model="estado">
      <option value="AC">Acre</option>
      <option value="AL">Alagoas</option>
      <option value="AP">Amapá</option>
      <option value="AM">Amazonas</option>
      <option value="BA">Bahia</option>
      <option value="CE">Ceará</option>
      <option value="DF">Distrito Federal</option>
      <option value="ES">Espírito Santo</option>
      <option value="GO">Goiás</option>
      <option value="MA">Maranhão</option>
      <option value="MT">Mato Grosso</option>
      <option value="MS">Mato Grosso do Sul</option>
      <option value="MG">Minas Gerais</option>
      <option value="PA">Pará</option>
      <option value="PB">Paraíba</option>
      <option value="PR">Paraná</option>
      <option value="PE">Pernambuco</option>
      <option value="PI">Piauí</option>
      <option value="RJ">Rio de Janeiro</option>
      <option value="RN">Rio Grande do Norte</option>
      <option value="RS">Rio Grande do Sul</option>
      <option value="RO">Rondônia</option>
      <option value="RR">Roraima</option>
      <option value="SC">Santa Catarina</option>
      <option value="SP">São Paulo</option>
      <option value="SE">Sergipe</option>
      <option value="TO">Tocantins</option>
    </select>

    <p>hobbies:</p>
    <input type="text" v-model="hobbies" placeholder="digite seus hobbies">

    <p>linguagem de programação:</p>
    <input type="text" v-model="linguagemp" placeholder="digite sua linguagem">
    <p>biografia:</p>
    <textarea type="text" v-model="biografia" cols="30" rows="10"></textarea>
</div>
</form>
</template>

<style scoped>
.estrutura{
  border: 5px solid rgb(0, 0, 0); 
  border-radius: 50px;
  text-align: center;
  padding: 50px;
  background-color: rgb(140, 142, 255);
  font-size: 18px;
  color: black;
}

</style>
