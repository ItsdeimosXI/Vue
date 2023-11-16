<template>
    <div>
        <h3> {{ counter }} </h3>
        <button @click="addCounter" class="btn btn-primary"> Incrementar</button>
    </div>
</template>
<script  lang="ts" setup>
import { Ref , ref } from 'vue';
        let counter:Ref = ref(0);
        const addCounter = ():void => {
            counter.value++
        }
</script>