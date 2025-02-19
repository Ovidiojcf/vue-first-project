<template>
  <div class="container">
    <div style="margin: 10px;">
      <input type="text" class="custom-input" v-model="name" placeholder="Type your name">
    </div>
    <div  style="margin: 5px;">
      <!--Utiliza :variavel para conciliar a reatividade da variavel-->
      <HelloPerson :name="name"/>
    </div>
    <div>
      
    </div>
  </div>
</template>
<!-- Para utilizar algum componente nessa página é necessário importa-lo na tag script-->
<script setup>
import { ref } from 'vue';
import HelloPerson from './components/HelloPerson.vue';
const name = ref("");

</script>

<style>
  .container{
    display: column;
    justify-content: space-between;
    font-family:
    Inter,
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    Oxygen,
    Ubuntu,
    Cantarell,
    'Fira Sans',
    'Droid Sans',
    'Helvetica Neue',
    sans-serif;
  }
  .custom-input{
    padding: 10px;
    border: 2px solid hsla(160, 100%, 37%, 1);
    border-radius: 5px;
    font-size: 40px;
  }
  .primary-button{
    font-size: 20px;
    background:  hsla(160, 100%, 37%, 0.2);
    border: 2px solid;
    border-radius: 5px;
    
  }
</style>