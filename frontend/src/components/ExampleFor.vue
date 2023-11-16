<template>
    <div>
        <ul class="list-group">
            <li class="list-group-item" v-for="pais in paises" v-bind:key="pais">
                {{ pais }}
            </li>
        </ul>
    </div>
</template>

<script setup lang="ts">
import { Ref, ref } from 'vue';
let paises: Ref<Array<string>> = ref([
    'Argentina',
    'España',
    'UK',
    'Portugal'
])
</script>

<style scoped></style>