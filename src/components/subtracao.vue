<script setup lang="ts">
import { ref } from 'vue'
const valorX = ref(0);
const valorY = ref(0);
const resultado = ref(0);

function sub(){
    resultado.value =valorX.value - valorY.value;
}
</script>


<template>
    <h2>subtração</h2>
    <div>
        <input type="number" v-model="valorX" placeholder="Digite o numero">

         <input type="number" v-model="valorY" placeholder="Digite o numero">
         <button @click="sub">Subtração</button>
    </div>
    <div>
        <p>Resultado é {{ resultado }}</p>
    </div>

</template>

<style></style>