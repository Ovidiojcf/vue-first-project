<template>
    <div class="cars">
        <h1>Bert Car</h1>
        <button class="primary-button" @click="acceleratePosition">
            Accelerate
        </button>
        <p class="p-increase">{{ props.position }}</p>
    </div>
</template>

<script setup>
    import { defineProps, defineEmits } from 'vue';

    const props = defineProps({ position: String });
    const emitPosition = defineEmits(['change-position']);

    /*Função necessária para o Bert falar que acelerou*/
    function acceleratePosition(){
        emitPosition('change-position');
    }
</script>


<style>
    .primary-button{
    font-size: 20px;
    border: 2px solid hsla(160, 100%, 37%, 1);
    border-radius: 5px;
    margin: 10px;
    padding: 10px;
    }
    .cars{
    display: flex;
    flex-direction: row;
    margin: 10px;
    }
    .p-increase{
        margin: 10px;
        font-size: 30px;
    }
</style>