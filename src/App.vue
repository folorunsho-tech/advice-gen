<script setup>
import AdviceVue from "./components/Advice.vue";
</script>

<template>
  <AdviceVue />
</template>

<style>
nav {
  padding: 1rem 0.5rem;
}
.profile {
  float: right;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: black;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: hsl(150, 100%, 66%);
  object-fit: cover;
}
</style>
