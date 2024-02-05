<script>
import { store } from '../../data/store.js';
import CharacterCard from '../charactercard.vue';
export default {
    name: 'CharactersList',
    data: () => ({ store }),
    components: { CharacterCard },
};
</script>

<template>
    <section id="characters">
        <div class="row">
            <div class="col" v-for="character in store.characters" :key="character._id">
                <CharacterCard v-bind="character" />
            </div>
        </div>
    </section>
</template>

<style></style>