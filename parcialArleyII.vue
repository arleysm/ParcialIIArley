<template>
  <div class="container">
    <h1 class="title">Parcial II Arley</h1>
    <div class="counter-group">
      <Mycounter :value="25" />
      <Mycounter2 :value="4" />
      <Mycounter3 :value="8" />
    </div>
    <div class="mouse-position">
      La Posición del Mouse es: <span>{{ x }}</span>, <span>{{ y }}</span>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Mycounter from './Components/MiCounter.vue';
import Mycounter2 from './Components/MiCounter2.vue';
import Mycounter3 from './Components/MiCounter3.vue';
import { useMouse } from './Composable.js';

const { x, y } = useMouse();
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #1b045a; 
  color: #021b16; 
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
  border: 2px solid #00ffcc; /* Borde neón */
}

.title {
  font-size: 2.5rem;
  margin-bottom: 20px;
  text-shadow: 0 0 10px rgba(238, 241, 241, 0.8);
}

.counter-group {
  display: flex;
  gap: 20px; /* Espaciado entre contadores */
  margin-bottom: 20px;
}

.mouse-position {
  font-size: 1.25rem;
  margin-top: 10px;
  background-color: #333; /* Fondo para la posición del mouse */
  color: #e9e6e6;
  padding: 10px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(141, 20, 20, 0.3);
}
</style>
