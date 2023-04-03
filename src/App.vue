<script setup>
import { ref } from 'vue'

const nome = ref('')
const email = ref('')
const senha = ref('')
const confirmaçãoDeSenha = ref('')
const dataDeNascimento = ref('')
const Endereço = ref('')
const Cidade = ref('')
const bio = ref('')
const hob = ref('')
const ativo = ref(true)
</script>

<template>
  <form>
  <div v-if="ativo === true">
    <input type="text" v-model="nome" placeholder="NOME" required/>
    <input type="email" v-model="email" placeholder="EMAIL" required/>
    <input type="password" v-model="senha" placeholder="SENHA" minlength="8" maxlength="20" required/>
    <input type="password" v-model="confirmaçãoDeSenha" placeholder="CONFIRMAÇÃO DA SENHA" required/>
    <input type="date" v-model="dataDeNascimento" placeholder="DATA DE NASCIMENTO" required/>
    <input type="number" v-model="Endereço" placeholder="ENDEREÇO" required/>
    <input type="text" v-model="Cidade" placeholder="CIDADE" required/> 
    <label for="estado">Estado:</label>
    <select required>
      <option value="nada"></option>
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
    <br>
    <label for="estado">Linguagens de programação:</label>
    <select>
      <option value="nada"></option>
      <option value="javascript">JavaScript</option>
      <option value="python">Python</option>
      <option value="java">Java</option>
      <option value="csharp">C#</option>
      <option value="php">PHP</option>
    </select>
    <br>
    <textarea v-model="hob" placeholder="ESCREVA ALGUNS HOBIES" cols="50" rows="10" />
    <br>
    <textarea v-model="bio" placeholder="ESCREVA SUA BIOGRAFIA" cols="100" rows="20" />
    <br>
    <button type="submit" @submit.prevent="">Tudo pronto</button>
  </div>
  <div v-else>
  </div>
</form>
</template>

<style scoped>
div {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

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

label {
  font-size: 16px;
  font-family: sans-serif;
  margin-bottom: 10px;
}

button {
        background-color: #3498db;
        border: none;
        border-radius: 10px;
        box-shadow: 0px 5px 0px #2980b9;
        color: #ffffff;
        font-size: 1.2rem;
        padding: 10px 20px;
        transition: all 0.3s ease-in-out;
      }

      button:hover {
        background-color: #2980b9;
        box-shadow: 0px 5px 0px #2c3e50;
        cursor: pointer;
      }

</style>
