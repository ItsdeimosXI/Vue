<template>
    <div>
        <p v-bind:class="{
            'danger': error
        }"> El mensaje ha sido enviado correctamente </p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
    name: 'ClassBind',
    data() {
        return {error: false
    }},
})
</script>

<style scoped>
.danger {
    color: red;
}
</style>