<template>
    <div class="person">
        <form>
        <div>
            <label for="name">Numele:</label>
            <span>{{person.name}}</span>
        </div>
        <div>
            <label for="mail">Mail:</label>
            <span>{{person.mail}}</span>
        </div>
        <div>
            <label for="nr">Telefonul:</label>
            <span>{{person.nr}}</span>
        </div>
        </form>    
    </div>
</template>

<script>

    export default {  
        props: {
            person: {
                type: Object,
                required: true
            }
        },
        data(){
            return {
                //product: {}
            }
        },   
    }    
</script>

<style scoped>
    .person {
        width: 500px;
        border: 1px solid black;
        margin: 10px;
        padding: 10px;  
    }
</style>