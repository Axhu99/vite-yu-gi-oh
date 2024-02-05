<script>
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
export default {
    name: 'CharactersList',
    data: () => ({
        characters: [],
    }),
    created() {
        axios.get(endpoint).then(res => {
            this.characters = res.data.docs;
        })
    }

};
</script>

<template>
    <section id="characters">
    </section>
</template>