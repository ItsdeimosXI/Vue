<template>
    <div>
        <form action="">
            <input type="text" v-model="inputext">
            <input type="checkbox" v-model="check">Acepto los termminos y condiciones
            <select v-model="paises">
                <option>Argentina</option>
                <option>Francia</option>
                <option>Estados Unidos</option>
                <option>Brasil</option>
                <option>Chile</option>
            </select>
        </form>
    </div>
    <h3> {{inputext}}</h3>
</template>

<script setup lang="ts">
import { Ref, ref } from 'vue';
let inputext:Ref<string> = ref('');
let check:Ref<boolean> = ref(true);
let paises= ref('Argentina');

</script>

<style scoped></style>