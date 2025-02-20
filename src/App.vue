<template>
  <div class="container">
    <div style="margin: 10px;">
      <input type="text" class="custom-input" v-model="name" placeholder="Type your name">
    </div>
    <div  style="margin: 5px;">
      <!--Utiliza :variavel sintaxe para conciliar a reatividade da variavel-->
      <HelloPerson :name="name"/>
    </div>
    <div>
      <IncreaseComponent @notificar="handleNotification" />
      <p class="p-increase">{{ message }}</p>
    </div>
    <!-- Carro do ovidio-->
    <div class="cars">
      <h1>Ovidio Car</h1>
      <button class="primary-button" @click="handlePosition()">
          Accelerate
      </button>
      <p class="p-increase">{{ position }}</p>
    </div>
    <!-- Carro do Bert-->
    <div>
      <carsDrive :position="position === 'Frente' ? 'Trás' : 'Frente'" @change-position="handlePosition()" />
    </div>
  </div>
</template>
<!-- Para utilizar algum componente nessa página é necessário importa-lo na tag script-->
<script setup>
  import { ref } from 'vue';
  import HelloPerson from './components/HelloPerson.vue';
  import IncreaseComponent from './components/IncreaseComponent.vue';
  import carsDrive from './components/carsDrive.vue';

  const name = ref("");
  const message = ref("");
  const position = ref("Frente");
  

  /*Funçãop necessária para o pai escutar o filho, sem ela o não é posivel receber a mensagem*/
  function handleNotification(msg) {
    message.value = msg;
  }
  /*Função necessária para o Ovídio escutar o bert caso ele acelere*/
  function handlePosition(){
    position.value = position.value === "Frente" ? "Atrás" : "Frente";
  }
  defineProps({
    
  })
  

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
    border: 2px solid hsla(160, 100%, 37%, 1);
    border-radius: 5px;
    font-size: 20px;
  }
  .p-increase{
        margin: 10px;
        font-size: 30px;
    }

  .cars{
    display: flex;
    flex-direction: row;
    margin: 10px;
  }
</style>