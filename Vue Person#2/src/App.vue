<template>
<div>
  <my-header></my-header>
  <div class="container">    
      <persons @viewDetails="viewDetails"></persons>
      <person-details :person="selectedPerson"></person-details>
  </div>
</div>
</template>

<script>
import PersonsList from './PersonsList.vue'
import PersonDetails from './PersonDetails.vue'
import myHeader from './Header.vue'

export default {
  data(){
    return {
      selectedPerson: {}
    }
  },
  components: {
    myHeader,
    'persons': PersonsList,
    PersonDetails,
  },  
  methods:{
    viewDetails(person){
      this.selectedPerson = person;
    }
  }
}
</script>

<style>
  .container{
    display:flex;
    align-items:flex-start;
  }
</style>
