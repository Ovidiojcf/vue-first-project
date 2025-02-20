<template>
    <div style="display: flex; flex-direction: column; gap: 15px;">
        <h1>Change the color</h1>
        <input type="color" v-model="corAnimal">
        <div  :style="{'background-color': corAnimal }" class="animal">
        </div>
    </div>
</template>
<script setup>
    import {ref} from 'vue';
    const corAnimal = ref('');
</script>
<style>
    .animal{
    width: 100px;
      height: 100px;
      clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
    }
</style>