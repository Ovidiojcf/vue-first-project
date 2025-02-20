<template>
    <div>
        <button class="primary-button" @click="increaseValue()">Increase by 1</button>
        <p class="p-increase">Count: {{ count }}</p>
    </div>
</template>

<script setup>
    import { ref } from 'vue';

    const emit = defineEmits(['notificar']);
    const count = ref(0);
    const maxLimit = 5;

    /*quando tem-se uma variavel reativa é necessário usar a sintaxe variavel.value++ para altera-la*/
    function increaseValue(){
        console.log('Increase Value is Activated')
        count.value++;
        if (count.value >= maxLimit) {
            notificarPai();
        }
    }

    function notificarPai(){
        emit('notificar', 'Alerta do Filho: count ultrapassou o valor!');
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
    .p-increase{
        margin: 10px;
        font-size: 30px;
    }
</style>