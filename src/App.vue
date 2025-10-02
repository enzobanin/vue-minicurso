<script setup>
  import PrimeiroComponente from './components/PrimeiroComponente.vue';
  import ComDados from './components/ComDados.vue';
  import ComDadosReativosPrimitivos from './components/ComDadosReativosPrimitivos.vue';
  import ComDadosReativosNaoPrimitivos from './components/ComDadosReativosNaoPrimitivos.vue';
  import DataBinding from './components/DataBinding.vue';
  import ComProps from './components/ComProps.vue';
  import EscutaEvento from './components/EscutaEvento.vue';

</script>

<template>
  <header>Vue</header>
  <EscutaEvento/>
  <ComProps item = "Borracha" :preco="2.50"/> <!-- usa-se o v-bind(:) para o preco não ser uma string>-->
  <!-- <ComProps item = "Lápis" :preco="1.25"/>
  <ComProps item = "Apontador" :preco="3.95"/> -->
  <DataBinding/>
  <ComDadosReativosNaoPrimitivos/>
  <ComDadosReativosPrimitivos/>
  <ComDados/>
  <PrimeiroComponente/>
  <!-- <PrimeiroComponente></PrimeiroComponente> pode escrever dessa maneira tambem--> 
</template>


