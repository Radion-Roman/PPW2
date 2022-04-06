<template>
    <div>
        <PersonItem v-for="(person, i) in persons" :key="person.id" :person="person" :index="(i+1)" @ViewDetails="ViewDetails"></PersonItem>
    </div>
</template>
<script>
    import PersonItem from './PersonItem.vue';
    import _ from 'lodash';

    export default {
        data(){
            return {
                persons: [
                    {
                        id: 1,
                        name: 'Person #1',
                    },
                    {
                        id: 2,
                        name: 'Person #2',
                    },
                    {
                        id: 3,
                        name: 'Person #3',
                    },
                    {
                        id: 4,
                        name: 'Person #4',
                    }                         
                ]
            }
        },
        components: {
            PersonItem
        },
        methods:{
           viewDetails(id){
                let personToView = _.find(this.persons, {id:id});
                this.$emit("viewDetails", personToView);
           } 
        }
    }
</script>