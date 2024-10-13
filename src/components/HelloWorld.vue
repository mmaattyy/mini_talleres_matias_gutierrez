<template>
  <div>
    <span>Nota 1:</span>
    <input v-model.number="nota1" type="number" step="0.01"><br><br>
    <span>Nota 2:</span>
    <input v-model.number="nota2" type="number" step="0.01"><br><br>
    <span>Nota 3:</span>
    <input v-model.number="nota3" type="number" step="0.01"><br><br>
    <span>Nota 4:</span>
    <input v-model.number="nota4" type="number" step="0.01"><br><br>
    <span>Nota 5:</span>
    <input v-model.number="nota5" type="number" step="0.01"><br><br>
    <span>Nota 6:</span>
    <input v-model.number="nota6" type="number" step="0.01"><br><br>
    <button @click="calcularPromedio">Calcular promedio</button><br><br>
    <span>El promedio es: {{ promedio.toFixed(2) }}</span>
  </div>
</template>

<script setup>
import { ref } from "vue";

const nota1 = ref(0);
const nota2 = ref(0);
const nota3 = ref(0);
const nota4 = ref(0);
const nota5 = ref(0);
const nota6 = ref(0);

const promedio = ref(0);

const calcularPromedio = () => {
  promedio.value = (nota1.value * 0.2
                    + nota2.value * 0.2
                    + nota3.value * 0.2
                    + nota4.value * 0.2
                    + nota5.value * 0.1
                    + nota6.value * 0.1);
}
</script>
