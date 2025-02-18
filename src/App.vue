<template>
  <firstComponent/>
</template>
<!-- Para utilizar algum componente nessa página é necessário importa-lo na tag script-->
<script>
  import firstComponent from './components/firstComponent.vue';
  export default{
    name: 'App',
    components:{
      firstComponent
    }
  }
</script>