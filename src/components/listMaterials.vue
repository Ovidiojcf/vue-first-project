<template>
    <h1>Displaying a list of items</h1>
    <button @click="mostrarMake()" class="primary-button">List Make</button>
    <button @click="mostrarModel()" class="primary-button">List Model</button>
    <ul v-if="exibir == true">
	    <li v-for="(car, index) in cars" :key="index">{{ car[tabela] }}</li>
    </ul>
</template>

<style>
    .primary-button{
        font-size: 20px;
        border: 2px solid hsla(160, 100%, 37%, 1);
        border-radius: 5px;
        font-size: 20px;
    }
</style>

<script setup>
    import {ref} from 'vue';

    const exibir = ref(false);
    const tabela= ref('');

    function mostrarMake(){
        tabela.value = 'make';
        console.log("mudando o valor de exibir");
        exibir.value = exibir.value ? false : true;
    }
    function mostrarModel(){
        tabela.value = 'model';
        console.log("mudando o valor de exibir");
        exibir.value = exibir.value ? false : true;
    }
    const cars = [
    {
        make: "Toyota",
        model: "Corolla",
        year: 2022,
        color: "Blue",
        engine: "1.8L I4",
        transmission: "Automatic",
        fuelType: "Gasoline",
        price: 25000
    },
    {
        make: "Honda",
        model: "Civic",
        year: 2021,
        color: "Red",
        engine: "2.0L I4",
        transmission: "Manual",
        fuelType: "Gasoline",
        price: 23000
    },
    {
        make: "Ford",
        model: "Mustang",
        year: 2023,
        color: "Black",
        engine: "5.0L V8",
        transmission: "Automatic",
        fuelType: "Gasoline",
        price: 45000
    },
    {
        make: "Tesla",
        model: "Model 3",
        year: 2022,
        color: "White",
        engine: "Electric",
        transmission: "Automatic",
        fuelType: "Electric",
        price: 50000
    },
    {
        make: "Chevrolet",
        model: "Camaro",
        year: 2021,
        color: "Yellow",
        engine: "3.6L V6",
        transmission: "Automatic",
        fuelType: "Gasoline",
        price: 35000
    }
    ];

</script>