<template>
    <div class="componente">
        <h1>Componente com Slots</h1>
        <button>
            <slot name="icone"></slot> 
            <slot name="texto">Botão</slot> <!--valor padrão para caso não passe nada -->
        </button>
    </div>
</template>