<template>
    <div class="person">
        <h2>Person Detail</h2>
        <form>
        <div>
            <label for="name">name:</label>
            <span>{{person.name}}</span>
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
            }
        },   
    }    
</script>

<style scoped>
    .person {
        width: 500px;
        border: 1px solid black;  
    }
</style>