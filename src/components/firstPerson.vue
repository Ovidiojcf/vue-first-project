<template>
    <h1>This is the description of that person: {{ name }}</h1>
    <infoComponent/>
</template>
<!-- No caso de hieraquias de componentes estou trazendo outras informações para o firstPerson, e ele é chamado na minha página App.vue-->
<script>
    import infoComponent from './infoComponent.vue';
    export default{
        name: 'firstPerson',
        components: {
            infoComponent
        },
        data(){
            return{
                name: 'Napoleão',

            }
        }
    }
</script>