<template>
    <div class="componente">
        <h1>Componente Com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{ pessoa.nome }}| Idade: {{ pessoa.idade }}</p>
        <button @click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<!-- <script setup>
import {reactive} from "vue";

    const pessoa = reactive({nome:"Enzo", idade:21}) 


    function fazerAniversario(){
        pessoa.idade +=1
    }
    function mudarNome(){
        pessoa.nome = "Enzo Banin"
    }
</script> -->

<script>
    export default{
        data:function(){
            return{ //tudo dentro do return, o vue sabe que pode mudar 
                pessoa:{
                    nome:"Enzo",
                    idade:21
                }
            }
        },
        methods:{
            fazerAniversario:function(){
                this.pessoa.idade += 1;
            },
            mudarNome:function(){
                this.pessoa.nome = "Enzo Banin";
            }
        }
    }
</script>

