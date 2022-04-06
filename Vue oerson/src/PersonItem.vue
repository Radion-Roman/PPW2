<template>
    <div class="pers">
        <div class="pers-body">
            <h4 class="pers-name">{{index}} {{person.name}}</h4>
            <a href="#" class="btn btn-primary" @click="viewDetailsClicked">View</a>            
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
</style>