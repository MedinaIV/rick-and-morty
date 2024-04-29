<script setup>
    const personagens = defineProps(["name", "url", "status", "especie", "genero", "localizacao", "episodio"])
    
</script>

<template>
    <div class="col-md-4">
        <div class="card mb-3">
            <img :src="personagens.url" alt="..." class="card-img-top">
            <div class="card-body">
                <p class="card-title text-center">Nome - {{ personagens.name }}</p>
                <p class="card-title text-center">Status - {{ personagens.status }}</p>
                <p class="card-title text-center">Espécie - {{ personagens.especie }}</p>
                <p class="card-title text-center">Gênero - {{ personagens.genero }}</p>
                <p class="card-title text-center">Localização Atual - {{ personagens.localizacao }}</p>
                <p class="card-title text-center">Participou -  {{ personagens.episodio }} Episódio</p>
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