<template>
    <div class="componente">
        <h1>Componente com Data Binding</h1>
        <p>{{ valor }}</p>
        <!-- ONE WAY DATA BINDING <input type="text" v-bind:value="valor"></input> -->
        <!-- TWO WAY DATA BINDING<input type="text" v-bind:value="valor" v-on:input="(event)=> valor = event.target.value"></input> -->
        <!-- COM ATALHOS <input type="text" :value="valor" @input="(event)=> valor = event.target.value"></input>-->
        <input type="text" v-model="valor"></input>
    </div>
</template>

<script setup>
    import {ref} from "vue";
    const valor = ref("Vue é um bom framework");
</script>