<script>
   import Card from './Card.vue';
   
   export default {
   data() {
     return {
      
     // SCRIVERE CHIAMATA API , METTERLO DENTRO UN ARRAY IN STORE, IN RIGHA 17 CARICARE ELEMENTI ARRAY INSTORE 
     } 
   }, 
   components: {
     Card
   }
}
</script>
<template>
    <div class="cards">
        <Card v-for="(card, i) in store.card" :key='i' :name="card.name" :archetype="card.archetype"
            :image="card.image" />
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;
  .cards{
        display: flex;
        flex-wrap: wrap;
        gap: 25px;
    }
</style>
