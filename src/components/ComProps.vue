<template>
    <div class="componente">
        <h1>Componente com Props</h1>
        <p>{{ item }}(R${{ preco.toFixed(2) }})</p>
    </div>
</template>

<script setup>
    import { defineProps } from 'vue';

    defineProps({ //define as propriedades que o componente vai receber
        item: String,
        preco: Number
    })

    // const item = "ooo" , mesma forma de usar do defineProps
</script>