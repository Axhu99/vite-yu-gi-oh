<script>
import CharactersList from './characters/characterslist.vue';
export default {
    name: 'AppMain',
    components: { CharactersList }
}
</script>

<template>
    <main class="container">
        <CharactersList />
    </main>
</template>
