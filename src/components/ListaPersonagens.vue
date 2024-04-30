<script setup>
    const personagens = defineProps(["name", "url", "status", "especie", "genero", "localizacao", "episodio"])
    
</script>

<template>
    <div class="col-md-4">
        <div class="card mb-3">
            <img :src="personagens.url" alt="..." class="card-img-top">
            <div class="card-body">
                <p class="card-title text-center">Name - {{ personagens.name }}</p>
                <p class="card-title text-center">Status - {{ personagens.status }}</p>
                <p class="card-title text-center">Specie - {{ personagens.especie }}</p>
                <p class="card-title text-center">Gender - {{ personagens.genero }}</p>
                <p class="card-title text-center">Location - {{ personagens.localizacao }}</p>
                <p class="card-title text-center">Appeared -  {{ personagens.episodio }} Episode</p>
            </div>
        </div>
    </div>
</template>

<style>
    .card-body{
        background-color: rgb(252, 254, 253);
        color: rgb(21, 110, 18);
        font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    }
</style>