<script>
   import {store} from '../store.js';
   import Card from './Card.vue';
   import axios from 'axios';
   
   export default {
   data() {
     return {
      store
     // SCRIVERE CHIAMATA API , METTERLO DENTRO UN ARRAY IN STORE, IN RIGHA 17 CARICARE ELEMENTI ARRAY INSTORE 
     } 
   }, 
   mounted(){
      this.fetchCard()
   },
   methods: {

    async fetchCard() {
    try {
        const url = 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=100&offset=0';
        const response = await axios.get(url);
        this.store.cards = response.data.data.map(card => ({
            name: card.name,
            archetype: card.archetype,
            image: card.card_images[0].image_url
        }));
        console.table(this.store.cards);
        console.log(this.store.cardsLength);
    } catch (error) {
        console.error('non riuscito a caricare', error);
    }
}
},
   components: {
     Card
   }
}
</script>
<template>
    <div class="cards container">
        <Card v-for="(card, i) in store.card" :key='i' :name="card.name" :archetype="card.archetype"
            :image="card.image"/>
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
