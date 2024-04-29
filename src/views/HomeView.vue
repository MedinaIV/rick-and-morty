<script setup>
import {ref, reactive, onMounted } from 'vue';
import listaCharacter from '../components/ListaPersonagens.vue';

let personagens = reactive(ref())


onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character?")
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results
    console.log(personagens)
  });
})

</script>


<template>
  <main>
    <div class="container">
      <div class="row mt-4">
        <listaCharacter
        v-for="character in personagens"            
        :key="character.name"
        :name="character.name"
        :url="character.image"
        :status="character.status"
        :especie="character.species"
        :genero="character.gender"
        :localizacao="character.location.name"
        >
        </listaCharacter>
      </div>  
    </div>
  </main>
</template>
