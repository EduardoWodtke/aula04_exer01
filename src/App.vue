<script setup>
import { ref } from 'vue'

const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmaçãoDeSenha = ref('')
const dataDeNascimento = ref('')
const Endereço = ref('')
const Cidade = ref('')
</script>

<template>
  <div >
    <input type="text" v-model="nome" placeholder="Nome" />
    <input type="email" v-model="email" placeholder="email" />
    <input type="password" v-model="senha" placeholder="senha" />
    <input type="password" v-model="confirmaçãoDeSenha" placeholder="Confirmação de senha" />
    <input type="date" v-model="dataDeNascimento" placeholder="Data de nascimento" />
    <input type="number" v-model="Endereço" placeholder="Endereço" />
    <input type="text" v-model="Cidade" placeholder="Cidade" />
    <label for="estado">Estado:</label>
    <select>
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
  </div>
</template>

<style scoped>
/* Estiliza o contêiner pai do formulário */
div {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

/* Estiliza os campos do formulário */
input, select {
  width: 300px;
  height: 30px;
  margin-bottom: 10px;
  border: none;
  border-bottom: 2px solid black;
  font-size: 16px;
  font-family: sans-serif;
  padding-left: 5px;
  box-sizing: border-box;
}

/* Estiliza o rótulo do campo Estado */
label {
  font-size: 16px;
  font-family: sans-serif;
  margin-bottom: 10px;
}

/* Estiliza o botão de envio do formulário */
button {
  width: 150px;
  height: 40px;
  margin-top: 20px;
  background-color: blue;
  color: white;
  font-size: 16px;
  font-family: sans-serif;
  border: none;
  cursor: pointer;
}

/* Estiliza o botão de envio do formulário quando o mouse passa por cima dele */
button:hover {
  background-color: darkblue;
}


</style>
