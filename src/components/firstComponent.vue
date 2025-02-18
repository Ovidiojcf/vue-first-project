<template>
    <h1>Hello Ovídio! How is it going?</h1>
    <div>
        <h1>If you're upset {{ name }}, don't worry. Everything it's gonna be okay!!</h1>
        <h1>You will become a {{ profession }}</h1>
    </div>
</template>
<!--Após a tag tamplate, sempre é necessário exportar o componente-->
<script>
    export default{
        name: 'firstComponent',
        data(){
            return{
                name:"Ovídio",
                profession: "Dev Front-End"
            }
        }
    }
</script>