<template>
    <div class="d-flex flex-row bd-highlight mb-3">
        <div class="p-2 bd-highlight">
        <ul class="list-group">
            <li class="list-group-item" v-for="pais in paises" :key="pais.code">
                {{ pais.name }}
            </li>
        </ul>
    </div>
    <div class="p-2 bd-highlight">
        <ul class="list-group">
            <li class="list-group-item" v-for="pais in paises" :key="pais.name">
                {{ pais.code }}
            </li>
        </ul>
    </div>
</div>
</template>

<script setup lang="ts">
import { Ref, ref } from 'vue';
interface IPaises{
    code: string,
    name: string
}
let paises:Ref<Array<IPaises>> = ref([
    {
        code: 'es',
        name: 'España'
    },
    {
        code: 'Fr',
        name: 'Francia'
    },
    {
        code: 'Ar',
        name: 'Argentina'
    },
    {
        code: 'EEUU',
        name: 'Estados Unidos'
    },
    {
        code: 'MX',
        name: 'Mexico'
    },
])
</script>

<style scoped></style>