<template>
    <div class="article-detail" v-if="article">
      <h1>{{ article.title }}</h1>
      <div class="article-meta">
        <span class="author">By: {{ article.summary }}</span>
        <span class="date">Date: {{ article.date }}</span>
            <!-- {{ new Date(article.date).toLocaleDateString() }}</span> -->
      </div>
      <img :src="article.thumbnail" :alt="article.title" class="article-image2">
      <div class="article-content">
        {{ article.thumbnail }}
        there will be content here one day
      </div>
    </div>


  </template>
  
  <script setup>
  import { ref } from 'vue';
  import { useRoute } from 'vue-router';
  
  const articles = [{    id: 1,
    title: "The Founding of Rome", 
    date: "April 21, 753 BC", 
    summary: "Legend says Rome was founded by Romulus in 753 BC in an area surrounded by seven hills.",
    thumbnail: "../src/assets/images/pik12.jpg"
  },
  { 
    id: 2,
    title: "The Pounding of Chrome", 
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
]
  
  const route = useRoute();
  const article = ref(articles.find(a => a.id === +route.params.id));
  </script>
  
  <style scoped>
  .article-detail {
      font-family: 'Roboto', sans-serif;
      max-width: 90%;
      margin: 40px auto;
      padding: 20px;
      background-color: #f4f4f4; 
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
      line-height: 1.7;
  }
  
  .article-detail h1 {
      font-size: 2.5em;
      color: #2C3A47;
      margin-bottom: 20px;
      font-weight: 500;
  }
  
  .article-meta {
      display: flex;
      justify-content: space-between;
      font-size: 0.9em;
      color: #636e72;
      margin-bottom: 30px;
  }
  
  .article-content {
      font-size: 1.2em;
      color: #333;
  }

  .article-image {
    align-self: center;
    max-width: 100%;
    height: auto;
    margin-bottom: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.article-image2 {
    width: 100%;
    height: 400px;
    object-fit: cover;
    margin-bottom: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1);
  }
  </style>
  