<script setup>
import AdviceVue from "./components/Advice.vue";
</script>

<template>
  <main class="main">
    <a target="_blank" href="https://github.com/folorunsho-tech/advice-gen"
      >View Code here-->></a
    >
    <AdviceVue />
  </main>
</template>

<style>
.main {
  width: 100%;
  display: flex;
  flex-direction: column;
}
.main > a {
  color: white;
  text-align: center;
  padding-top: 2rem;
}
</style>
