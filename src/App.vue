<script>
import axios from 'axios';
import { store } from './data/store.js';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons';
import AppMain from './components/AppMain.vue';
export default {
  name: 'Pokedex',
  components: { AppMain },
  methods: {
    /* metodo che chiama API e manda allo store un array di oggetti con alcune proprieta' (quelle utilizzate) */
    fetchCharacters() {
      axios.get(endpoint).then(res => {
        store.characters = res.data.docs.map(character => {
          return {
            id: character._id,
            name: character.name,
            number: character.number,
            type1: character.type1,
            imageUrl: character.imageUrl
          }
        });
      })
    },
  },
  /* Alla creazione chiamiamo il metodo */
  created() {
    this.fetchCharacters();
  }
};

</script>

<template>
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>