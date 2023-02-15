<template>
  <div>
  <Header :esta_logado="true"/>
    <PrimeiroComponente/>
    <p>O dado de app é: {{ testando }}</p>
    <LifeCycle/>
    <Pessoa/>
  </div>
</template>

<script>
import Header from "./components/form/Header.vue";
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import LifeCycle from "./components/LifeCycle.vue";
import Pessoa from "./components/Pessoa.vue";

export default {
  name: "App",
  components: {
    PrimeiroComponente,
    LifeCycle,
    Pessoa,
    Header
  },
};
</script>

<style  >

</style>
