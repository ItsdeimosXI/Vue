<template>
    <div class="p-2 bd-highlight">
        <h3>{{ props.titulo }}</h3>
        <p>{{ props.contenido }}</p>
        <img src="../assets/XDD.png" alt="XD">
        <input type="text" v-model="mensaje">
        <button class="btn btn.primary" @click="Click">Di hola</button>
    </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits, Ref, ref } from 'vue';

const props = defineProps(
    { titulo: String,
     contenido: String}
)

const emit = defineEmits(
    ['Dihola']
)
const Click = () => {
    emit("Dihola", mensaje.value)
}
let mensaje: Ref<string> = ref("")

</script>

<style scoped></style>