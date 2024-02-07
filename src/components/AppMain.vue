<script>
import CharactersList from './characters/CharactersList.vue';
export default {
    name: 'AppMain',
    components: { CharactersList },
}
</script>

<template>
    <main class="container">
        <CharactersList />
    </main>
</template>

<style>
.container {
    max-width: 1000px;
}
</style>