<template>
  <firstComponent/>
  <lifeCycle/>
</template>
<!-- Para utilizar algum componente nessa página é necessário importa-lo na tag script-->
<script>
  import firstComponent from './components/firstComponent.vue';
  import lifeCycle from './components/lifeCycle.vue';
  export default{
    name: 'App',
    components:{
      firstComponent,
      lifeCycle
    }
  }
</script>