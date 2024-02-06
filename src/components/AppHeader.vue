<script>
import SearchSelect from './SearchSelect.vue';

export default {
    name: 'AppHeader',
    data: () => ({
        types: ["Bug", "Dark", "Dragon", "Electric", "Fairy", "Fighting", "Fire", "Flying", "Ghost", "Grass", "Ground", "Ice", "Normal", "Poison", "Psychic", "Rock", "Steel", "Water"],
        searchType: '',
    }),
    emits: ['submit-value'],
    components: { SearchSelect }
}
</script>

<template>
    <select class="form-select base-form" v-model="searchType" @click="$emit('submit-value', searchType)">
        <option v-for=' type  in  types ' v-bind:value="type">{{ type }}</option>
    </select>
</template>

<style>
.base-form {
    width: 200px;
}
</style>
