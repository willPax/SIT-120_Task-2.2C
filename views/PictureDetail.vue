<template>
  <div class="picture-detail" v-if="picture">
    <h1>Title for {{ picture.id }}</h1>
    <img :src="picture.src" :alt="picture.alt" class="detail-image">
    <p>About for pik {{ picture.alt }}</p>
  </div>
</template>


<script setup>
import { ref } from 'vue';
import { useRoute } from 'vue-router';

const pictures = 
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
];

const route = useRoute();

const picture = ref(pictures.find(p => p.id === +route.params.id));
</script>

<style scoped>
.picture-detail {
    font-family: 'Roboto', sans-serif;
    max-width: 800px;
    margin: 40px auto;
    padding: 20px;
    text-align: center;
    background-color: #f4f4f4; 
    border-radius: 15px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
    line-height: 1.7;
}

.picture-detail h1 {
    font-size: 2.2em;
    color: #2C3A47;
    margin-bottom: 20px;
    font-weight: 500;
}

.picture-detail p {
    font-size: 1.2em;
    color: #636e72;
}
.detail-image {
    max-width: 100%;
    height: auto;
    margin-bottom: 20px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
}
</style>