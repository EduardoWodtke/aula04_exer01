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
const linPrograma = ref([])
</script>

<template>
  <form>
  <h1>Ganhe robux</h1>
  <div v-if="ativo === true">
    <input id="inpu" type="text" v-model="nome" placeholder="NOME" required/>
    <input id="inpu" type="email" v-model="email" placeholder="EMAIL" required/>
    <input id="inpu" type="password" v-model="senha" placeholder="SENHA" minlength="8" maxlength="20" required/>
    <input id="inpu" type="password" v-model="confirmaçãoDeSenha" placeholder="CONFIRMAÇÃO DA SENHA" required/>
    <input id="inpu" type="date" v-model="dataDeNascimento" placeholder="DATA DE NASCIMENTO" required/>
    <input id="inpu" type="number" v-model="Endereço" placeholder="ENDEREÇO" required/>
    <input id="inpu" type="text" v-model="Cidade" placeholder="CIDADE" required/> 
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
    <label for="LinProgramação">Linguagens de programação: 
      <input id="check" type="checkbox" v-model="linPrograma" value="PHP"> PHP
      <input id="check" type="checkbox" v-model="linPrograma" value="JS"> JS
      <input id="check" type="checkbox" v-model="linPrograma" value="C++"> C++
      <input id="check" type="checkbox" v-model="linPrograma" value="Python"> Python     
    </label>  
    <br>
    <textarea v-model="hob" placeholder="ESCREVA ALGUNS HOBIES" cols="50" rows="10" />
    <br>
    <textarea v-model="bio" placeholder="ESCREVA SUA BIOGRAFIA" cols="100" rows="20" />
    <br>
    <button @click="ativo" type="submit" >Tudo pronto</button>
  </div>
</form>
<div v-if="ativo === false">
<p>{{ nome }}</p>
<p>{{ email }}</p>
<p>{{ senha }}</p>
<p>{{confirmaçãoDeSenha}}</p>
<p>{{dataDeNascimento}}</p>
<p>{{Endereço}}</p>
<p>{{ Cidade }}</p>
<p>{{ linPrograma }}</p>
<p>{{ bio }}</p>
<p>{{ linPrograma }}</p>
</div>
</template>

<style scoped>
div {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

#inpu, select {
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
