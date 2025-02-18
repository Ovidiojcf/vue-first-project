<template>
    <h1>My name is: {{ name }}</h1>
</template>

<script>
    export default{
        name: 'lyfeCyvel',
        data(){
            return{
                name: 'Doesnt know'
            }
        },
        created(){
            setTimeout(()=>{
                this.name = 'Ovidio'}, 1000
            );
        },
        mounted(){
            this.name = 'José'
        }
    }
</script>