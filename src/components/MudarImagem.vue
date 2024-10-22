<template>
    <div>
        <button @click="$emit('trocaImagem')">Trocar imagem de perfil</button>
    </div>
</template>

<script>
    export default {
        name: 'MudarImagem',
        emits: ['trocaImagem']
    }
</script>