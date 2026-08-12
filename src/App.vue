<script setup lang="ts">
import {ref} from'vue';
import Soma from './components/soma.vue'
import Subtracao from './components/subtracao.vue'
import Divisao from './components/divisao.vue';
import Multiplicar from './components/multiplicar.vue';

let showSoma = ref(false)
let showSub = ref(false)
let showMult = ref(false)
let showDiv = ref(false)


function soma(){
  showSoma.value = true;
  showSub.value = false;
  showMult.value = false;
  showDiv.value = false;
}
function sub(){
  showSoma.value = false;
  showSub.value = true;
  showMult.value = false;
  showDiv.value = false;
}
function mult(){
  showSoma.value = false;
  showSub.value = false;
  showMult.value = true;
  showDiv.value = false;
}
function div(){
  showSoma.value = false;
  showSub.value = false;
  showMult.value = false;
  showDiv.value = true;
}

</script>

<template>
  <h1>Calculadora</h1>
  <p>
   Execute as quatro operações básicas 
  </p>
  <div>
    <h2>Escolha a numeração: </h2>
    <button @click="soma">+</button>
    <button @click="sub">-</button>
    <button @click="mult">*</button>
    <button @click="div">/</button>
  </div>

  <Soma v-if="showSoma"/>
 
   <Subtracao v-if="showSub"/>
    <Divisao v-if="showDiv"/>
    <Multiplicar v-if="showMult"/>

  
</template>


<style >
*{
  background-color: #ee91e2;
}
</style>