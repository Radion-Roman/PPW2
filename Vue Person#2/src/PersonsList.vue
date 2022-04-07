<template>
    <div>
        <PersonItem v-for="(person, i) in persons" :key="person.id" 
        :person="person" :index="(i+1)" @viewDetails="viewDetails"></PersonItem>
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
                        work: "Mihai Eminescu",
                        name: "Ioan Mircea",
                        mail: "Ioan@gmail.com",
                        nr: "01234573"
                    },
                    {
                        id: 2,
                        work: "Grigorie Vieru",
                        name: 'Alexandru Popescu',
                        mail: "Alexandru@bk.ru",
                        nr: "012345671"
                    },
                    {
                        id: 3,
                        work: "Alexandr Pushkin",
                        name: 'Timofei Alexandrovici',
                        mail: "Timofei@mai.ru",
                        nr: "086745362"
                    },
                    {
                        id: 4,
                        work: "Ion Creanga",
                        name: 'Andrei Timofeivici',
                        mail: "Andrei@gmail.com",
                        nr: "045643456"
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