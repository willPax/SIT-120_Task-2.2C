<script setup>
import { ref } from 'vue'

import ArticlesComponent from '../components/ArticlesComponent.vue'


const moreArticles = ref([
  { 
    id: 1,
    title: "The Founding of Rome", 
    date: "April 21, 753 BC", 
    summary: "Legend says Rome was founded by Romulus in 753 BC in an area surrounded by seven hills.",
    thumbnail: "../src/assets/images/pik12.jpg"
  },
  { 
    id: 2,
    title: "The Pounding of Chome", 
    date: "April 21, 753 BC", 
    summary: "Legend says Rome was founded by Romulus in 753 BC in an area surrounded by seven hills.",
    thumbnail: "../src/assets/images/pik8.jpg"
  },  { 
    id: 3,
    title: "The Sounding of Drone", 
    date: "April 21, 753 BC", 
    summary: "Legend says Rome was founded by Romulus in 753 BC in an area surrounded by seven hills.",
    thumbnail: "../src/assets/images/pik5.jpg"
  },
  { 
    id: 4,
    title: "Moon Landing", 
    date: "July 20, 1969", 
    summary: "Neil Armstrong becomes the first human to step on the surface of the Moon.",
    thumbnail: "../src/assets/images/pik2.jpg"
  },
])


</script>

<template>
    <div class="main-heading">
    <h1>Chronicles of the Past</h1>
    <p>Dive deep into well-researched articles that recount the tales and events of yesteryears.</p>
    </div>

    <ArticlesComponent :articles="moreArticles"/>
</template>

