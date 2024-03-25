<script setup>
import { ref } from 'vue'

const nome = ref('')
const sexo = ref('')
const cidade = ref('')
const estado = ref('')
const email = ref('')
const senha = ref('')
const data = ref('')
const confirmar = ref('')

function Confirmar(){
  if(nome.value.length < 3){
    alert("O nome deve ter mais de 3 letras")
    return false;
  }
  if(!email.value.includes("@")){
    alert("O e-mail deve ser váli do")
    return false;
  }
  if(senha.value != confirmar.value){
    alert("Senha errada.")
  }
  if(cidade.value == ""){
    alert("coloque sua cidade. ")
  }

}
</script>

<template>
<div class="formu">
    <form action="">
    <p>nome</p>
    <input type="text" v-model="nome" />

    <p>senha</p>
    <input type="password" v-model="senha" minlength="3" />

    <p>Confirmar senha</p>
    <input type="password" v-model="confirmar" minlength="3" />

    <p>email</p>
    <input type="email" v-model="email" />

    <p>idade</p>
    <input type="number" v-model="idade" />


    <p>data</p>
    <input type="date" v-model="data" />
  
    <p>endereço</p>
    <input type="text" v-model="endereço" /> 

    <button type="button" @click="Confirmar()">Confirmar</button>
    
      <p>Estado</p>
    <select v-model="estado">
      <option value="AC">AC</option>
      <option value="AL">AL</option>
      <option value="AP">AP</option>
      <option value="AM">AM</option>
      <option value="BA">BA</option>
      <option value="CE">CE</option>
      <option value="DF">DF</option>
      <option value="ES">ES</option>
      <option value="GO">GO</option>
      <option value="MA">MA</option>
      <option value="MT">MT</option>
      <option value="MS">MS</option>
      <option value="MG">MG</option>
      <option value="PA">PA</option>
      <option value="PB">PB</option>
      <option value="PR">PR</option>
      <option value="PE">PE</option>
      <option value="PI">PI</option>
      <option value="RJ">RJ</option>
      <option value="RN">RN</option>
      <option value="RS">RS</option>
      <option value="RO">RO</option>
      <option value="RR">RR</option>
      <option value="SC">SC</option>
      <option value="SP">SP</option>
      <option value="SE">SE</option>
      <option value="TO">TO</option>

    </select>

      <p>Hobbie</p>
    <select v-model="estado">
      <option value="esporte">masculino</option>
      <option value="leitura">feminino</option>
      <option value="cozinhar"></option>
      <option value="estudar"></option>
      <option value="games">games</option>
    </select>

  <p>Sexo</p>
    <select v-model="sexo">
      <option value="masculino">masculino</option>
      <option value="feminino">feminino</option>
    </select>


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
