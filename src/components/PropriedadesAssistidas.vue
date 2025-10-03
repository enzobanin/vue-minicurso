<template>
    <div class="componente">
        <h1>Componente com Propriedades Assistidas</h1>
        <p>Idade:{{ idade }}</p>
        <label>Ano Nascimento: </label>
        <input type="number" v-model="anoNascimento" min="1900">
        <label>Ano Atual: </label>
        <input type="number" v-model="anoAtual" min="2000">
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    // import { watch } from 'vue';
    import { watchEffect } from 'vue';

    const anoNascimento = ref(1900)
    const anoAtual = ref(2000)
    const idade = ref(0)

    // watch(anoAtual,(ano)=>{ //observa se o anoAtual mudar e vai receber o novo anoAtual (ano) por parametro, executando o callback, atualizando a idade                     
    //     idade.value = ano - anoNascimento.value
    // })
    // watch(anoNascimento,(ano)=>{
    //     idade.value = anoAtual.value - ano
    // })
    // o watch nao seria tão util pois essas funcoes sao praticamente as mesmas, seria útil: fazer requisicao para uma API externa, mudar a DOM
    watchEffect(()=>{ //não precisa especificar qual variavel a gente esta monitorando
        idade.value = anoAtual.value - anoNascimento.value
    })
    //idade é um dado armazenado(ref) então ele não se atualiza sozinho, por isso usamos o watchEffect para observar se há alguma mudanca e assim atualizar a idade
</script>

<style scoped>
    label{
        margin: 10px;
    }
</style>