<template>
    <div class="pers">
        <div class="pers-body">
            <h4 class="pers-title"> {{person.work}}</h4>
            <a href="#" class="btn btn-primary" @click="viewDetailsClicked"></a>            
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            person: {
                type: Object,
                required: true,
            },
            index: {
                type: Number,
            }
        },
        data(){
            return{
                //product: {},
                //index: 1
            }
        },
        methods: {
            viewDetailsClicked(){
                this.$emit("viewDetails",this.person.id);
            }
        }
    }
</script>

<style>
    div.pers {
        width: 200px;
        border: 1px solid black;
    }
    .btn-primary{
        width: 150px;
        background-color: black ;
        border-color: black ;
    }
    .btn-primary:focus{
        width: 150px;
        background-color: cadetblue;
        border-color: black ;
    }
    .btn-primary:hover{
        width: 150px;
        background-color: blueviolet;
        border-color: black ;
    }
</style>