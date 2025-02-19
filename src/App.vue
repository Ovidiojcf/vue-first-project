<template>
  <firstComponent/>
  <lifeCycle/>
  <div>
    <firstPerson/>
  </div>
</template>
<!-- Para utilizar algum componente nessa página é necessário importa-lo na tag script-->
<script>
  import firstComponent from './components/firstComponent.vue';
  import lifeCycle from './components/lifeCycle.vue';
  import firstPerson from './components/firstPerson.vue';

  export default{
    name: 'App',
    components:{
      firstComponent,
      lifeCycle,
      firstPerson
    }
  }
</script>