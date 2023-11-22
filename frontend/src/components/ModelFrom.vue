<template>
    <div>
        <form action="">
            <input type="text" v-model="inputext">
        </form>
    </div>
    <h3> {{inputext}}</h3>
</template>

<script setup lang="ts">
import { Ref, ref } from 'vue';

let inputext:Ref<string> = ref('')
</script>

<style scoped></style>