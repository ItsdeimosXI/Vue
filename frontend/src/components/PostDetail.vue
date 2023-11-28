<template>
    <div class="p-2 bd-highlight">
        <h3>{{ props.titulo}}</h3>
        <p>{{ props.contenido}}</p>
        <img src="../assets/XDD.png" alt="XD">
        <input type="text" v-model="mensaje">
        <button class="btn btn.primary" @click="Click" >Di hola</button>
    </div>
</template>

<script lang="ts">
import { Ref, defineComponent, ref } from 'vue';

export default defineComponent({
    name: 'PostDetail',
    props: {
        titulo:{
            type: String,
            required: true
        },
        contenido:{
            type: String,
            required: false,
            default: 'Este post no tiene contenido'
        }
    },
    emits: ["Dihola"],
    setup(props, {emit} ) {
        const Click = () => {
           emit( "Dihola", mensaje.value)
        }
        let mensaje:Ref<string> = ref("")
        return {props, Click, mensaje}
    },
})
</script>

<style scoped>

</style>