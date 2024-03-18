<script setup>
import { ref } from 'vue'

const nome = ref('')
const sexo = ref('')
const cidade = ref('')
const estado = ref('')
</script>

<template>
<div class="formu">
    <form action="">
    <p>nome</p>
    <input type="text" v-model="nome" />

    <p>senha</p>
    <input type="password" v-model="senha" minlength="3" />

    <p>email</p>
    <input type="email" v-model="email" />

    <p>idade</p>
    <input type="number" v-model="idade" />

    <p>endereço</p>
    <input type="text" v-model="endereço" />
    
      <p>Cidade</p>
    <select v-model="cidade">
      <option value=""></option>
      <option value=""></option>
      <option value=""></option>
      <option value=""></option>
      <option value=""></option>
    </select>

      <p>Estado</p>
    <select v-model="estado">
      <option value="masculino">masculino</option>
      <option value="feminino">feminino</option>
    </select>

  <p>Sexo</p>
    <select v-model="sexo">
      <option value="masculino">masculino</option>
      <option value="feminino">feminino</option>
    </select>

    <p>data</p>
    <input type="date" v-model="data" />
  
    <button type="button">Confirmar</button>

    </form>

  </div>
</template>

<style>
input {
  margin: 10px;
}
p {
  text-align: center;
}
form{
  text-align: center;
}
.formu{
  background-color: rgb(229, 255, 246);
  width: 390px;
  text-align: center;
}
button{
  background-color: cornflowerblue;
}
</style>
