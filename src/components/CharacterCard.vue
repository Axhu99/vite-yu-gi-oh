<script>
export default {
    name: 'CharacterCard',
    props: {
        id: String,
        name: String,
        number: Number,
        type1: String,
        imageUrl: String,
    },
}
</script>

<template>
    <!-- TODO fare una card e controllare meglio l'immagine -->
    <!-- creo la carta con: l'immagine, il numero, il nome e il tipo del pokemon -->
    <div class="character-card text-center">
        <img :src="imageUrl" :alt="name" class="img-fluid rounded-circle mb-3">
        <div>{{ number }}</div>
        <h3>{{ name }}</h3>
        <div>{{ type1 }}</div> <!-- TODO mettere entrambi i tipi -->
    </div>
</template>

<style></style>