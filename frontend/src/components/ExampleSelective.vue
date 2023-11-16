<template>
    <div>
        <h1 v-if="age < 18"> Eres menor de edad</h1>
        <h1 v-else> Eres mayor de edad</h1>
    </div>
</template>

<script lang="ts" setup>
    let age:number = 18
</script>
