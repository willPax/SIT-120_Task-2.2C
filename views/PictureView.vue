<script setup>
import { ref } from 'vue'

import PicturesGrid from '../components/PicturesGrid.vue';


const piklist = ref(
[

{ id: 1, src: "../src/assets/images/pik1.jpg", alt: "Description 1" },
{ id: 2, src: "../src/assets/images/pik2.jpg", alt: "Description 2" },
{ id: 3, src: "../src/assets/images/pik3.jpg", alt: "Description 2" },
{ id: 4, src: "../src/assets/images/pik4.jpg", alt: "Description 2" },
{ id: 5, src: "../src/assets/images/pik5.jpg", alt: "Description 2" },
{ id: 6, src: "../src/assets/images/pik6.jpg", alt: "Description 2" },
{ id: 7, src: "../src/assets/images/pik7.jpg", alt: "Description 2" },
{ id: 8, src: "../src/assets/images/pik8.jpg", alt: "Description 2" },
{ id: 9, src: "../src/assets/images/pik9.jpg", alt: "Description 2" },
{ id: 10, src: "../src/assets/images/pik10.jpg", alt: "Description 2" },
{ id: 11, src: "../src/assets/images/pik11.jpg", alt: "Description 2" },
{ id: 12, src: "../src/assets/images/pik12.jpg", alt: "Description 2" },
]
)

 
</script>

<template>
    <div class="main-heading">
    <h1>Gallery of Wonders</h1>
    <p>Experience the timeless beauty of our exhibits through photographs.</p>
</div>
    

    <PicturesGrid :images="piklist" />
</template>

