<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Primitivos</h1>
        <p>Nome: {{ nome }}| Idade: {{ idade }}</p>
        <button @click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<script setup>
import {ref} from "vue";

    const nome = ref("Enzo");
    const idade = ref(21);
    
    function fazerAniversario(){
        idade.value +=1
        //this.idade = idade;
    }
    function mudarNome(){
        nome.value = "Enzo Banin"
        //this.nome = nome;
    }
</script>

