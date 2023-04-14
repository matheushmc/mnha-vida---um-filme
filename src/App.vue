<script setup>
import { ref } from 'vue'

const nome = ref('')
const email = ref('')
const senha = ref('')
const senha1 = ref('')
const data = ref('')
const endereço = ref('')
const cidade = ref('')
const estado = ref('')
const hobie = ref('')
const linguaguemp = ref('')
const biografia = ref('')

const mostrar = ref(false)

</script>

<template>

<form>
  <div class="corpo">
    <p>Nome: </p>
    <input type="text" v-model="nome" placeholder="Digite seu nome" />
    <p>Email: </p>
    <input type="email" v-model="email" placeholder="Digite seu email" />
    <p>Senha: </p>
    <input type="password" v-model="senha" placeholder="Digite sua senha" />
    <p>Confirmar senha: </p>
    <input type="password" v-model="senha1" placeholder="Digite sua senha" />
    <div v-if="senha === senha1">
      ta certa a senha
    </div>
    <div v-else>
      a senha ta errada
    </div>
    <p>Data de Nascimento;</p>
    <input type="date" v-model="data">
    <p>Endereço:</p>
    <input type="text" v-model="endereço" placeholder="rua;Nºda casa;">
    <p>Cidade:</p>
    <input type="text" v-model="cidade" placeholder="Digite seu Endereço">
    <p>Estado:</p>
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
    <p>Hobbies:</p>
    <input type="text" v-model="hobie" placeholder="Digite seus hobbies">
    <p>Linguagem de programação:</p>
    <select v-model="linguaguemp">
      <option value="JavaScript">JavaScript</option>
      <option value="C++">C++</option>
      <option value="Python">Python</option>
      <option value="Java">Java</option>
      <option value="C#">C#</option>
    </select>
    <p>Biografia:</p>
    <textarea v-model="biografia" cols="30" rows="10"></textarea>
  </div>
</form> 

<div class="salvas">
<button  @click="$event => mostrar = !mostrar"> 
  Informações Salvas
</button>
  <div v-if="mostrar">
    <div>
      <div>
        <div>
          nome:
        {{ nome }}
      </div>
      <div>
        email:
        {{ email }}
      </div>
      <div>
        senha:
        {{ senha }}
      </div>
      <div>
        data:       
        {{ data }}
      </div>
      <div>
        endereço:
        {{ endereço }}
      </div>
      <div>
        cidade:
        {{ cidade }}
      </div>
      <div>
        estado:
        {{ estado }}
      </div>
      <div>
        hobbies:
        {{ hobie }}
      </div>
      <div>
        linguegem de programação:
        {{ linguaguemp }}
      </div>
      <div>
        biografia:
        {{ biografia }}
      </div>
    </div>
  </div>
</div>
</div>

</template>

<style scoped>

form {
  grid-template-columns: 50% 50%;
  margin: 25px 25px 25px 25px;
}
.corpo {
  border: 5px solid rgb(0, 0, 0);
  border-radius: 50px;
  text-align: center;
  padding: 25px;
  background-color: rgb(92, 167, 177);
}

.salvas {
  text-align: center;
  padding: 25px;
}

</style>