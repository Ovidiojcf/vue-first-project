<template>
    <h1>Hello, {{name}}! Hope you're having a</h1>
    <h1 class="text-bold-green">great day!</h1>
</template>


<script setup>
defineProps({
    name: String,
});
</script>

<style>
    .text-bold-green{
        font-size: 70px;
        color: hsla(160, 100%, 37%, 1);
        font-weight: bold;
        text-align: start;
    }
</style>
