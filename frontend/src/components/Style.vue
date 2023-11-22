<template>
    <div>
        <p v-bind:style="{
            backgroundColor : 'white', color: color
        }"> El mensaje ha sido enviado correctamente </p>
        <button class="btn btn-primary" @click="Click">Cambiar color</button>
    </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent ({
    name: 'Click',
    data(){
        return{
            color: 'red'
        }
    },
    methods:{
        Click(){
            this.color = 'grey'
        }
    }
})

</script>

<style scoped>
.danger {
    color: red;
}
</style>