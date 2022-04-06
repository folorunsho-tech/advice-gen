<script setup>
import Dice from "./icons/icon-dice.vue";
import Divider from "./icons/pattern-divider-mobile.vue";
import { onMounted, ref } from "vue";
const advice = ref({});

const fetchAdvices = async () => {
  const data = await (await fetch("	https://api.adviceslip.com/advice")).json();
  advice.value = data.slip;
};
onMounted(async () => {
  await fetchAdvices();
});
</script>
<template>
  <div class="advice">
    <p>Advice #{{ advice.id }}</p>
    <q>{{ advice.advice }}</q>
    <Divider />
    <button class="random" @click="fetchAdvices"><Dice /></button>
  </div>
</template>
<style>
.advice {
  display: flex;
  flex-direction: column;
  margin: 8rem auto;
  gap: 0.8rem;
  justify-content: center;
  padding: 1rem 1.5rem;
  text-align: center;
  background-color: hsl(217, 19%, 24%);
  max-width: 300px;
  height: 300px;
  border-radius: 12px;
  position: relative;
}

.advice p {
  font-size: small;
  text-transform: uppercase;
  letter-spacing: 4px;
  color: hsl(150, 100%, 66%);
}

.advice q {
  font-size: 28px;
  color: hsl(193, 38%, 86%);
  font-weight: 800;
  margin-bottom: 5px;
}
.advice .random {
  background: hsl(150, 100%, 66%);
  border: none;
  vertical-align: middle;
  margin: auto;
  left: 41%;
  cursor: pointer;
  width: 60px;
  text-align: center;
  height: 60px;
  border-radius: 100%;
  position: absolute;
  bottom: -2rem;
}
</style>
