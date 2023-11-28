<template>
    <div class="d-flex flex-column bd-highlight mb-3">
        <PostDetail @Dihola="alerta" v-for="elm in info" :key="elm.titulo" 
        :titulo="elm.titulo" :contenido="elm.contenido"/>
    </div>
</template>

<script setup lang="ts">
import PostDetail from './PostDetail.vue';
interface Posts {
    titulo: string,
    contenido: string
}
let info: Array<Posts> = [
    {
        titulo: "Post 1",
        contenido: "Texto ejemplo 1"
    },
    {
        titulo: "Post 2",
        contenido: "Texto ejemplo 2"
    },
    {
        titulo: "Post 3",
        contenido: "Texto ejemplo 3"
    },
    {
        titulo: "Post 4",
        contenido: "Texto ejemplo 4"
    },
    {
        titulo: "Post 5",
        contenido: "Texto ejemplo 5"
    }]
function alerta(msg: string) {
    alert(msg)
}
</script>

<style scoped></style>