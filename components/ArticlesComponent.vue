
  <template>
    <section class="articles-section">
      <!-- <h1 class="section-title">Historical Articles</h1> -->
      <div class="articles">
        <div v-for="article in articles" :key="article.id" class="article-item">
        <span  @click="goToDetail(article.id)">
          <img v-if="article.thumbnail" :src="article.thumbnail" :alt="article.title" class="article-thumbnail"/>
          <div class="article-content">
            <h2 class="article-title">{{ article.title }}</h2>
            <p class="article-date">{{ article.date }}</p>
            <p class="article-summary">{{ article.summary }}</p>
          </div>
        </span>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { useRouter } from 'vue-router';
defineProps ({
    articles: Array
})
    const { push } = useRouter();

const goToDetail = (articleId) => {
  push(`/articles/${articleId}`);
};
  
  </script>
  
  <style scoped>
  .articles-section {
    font-family: 'Arial', sans-serif;
    background-color: #ffffff;
    padding: 40px 20px;
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .section-title {
    text-align: center;
    font-size: 2.5em;
    margin-bottom: 50px;
    color: #333;
  }
  
  .articles {
    display: flex;
    flex-wrap: wrap;
    gap: 20px; /* For space between items */
    justify-content: center; /* Center items on smaller screens */
  }
  
  .article-item {
    flex: 1 1 calc(33.333% - 20px); /* Three articles per row, considering the gap */
    box-sizing: border-box;
    margin-bottom: 40px;
    padding: 20px;
    border: 1px solid #eee;
    border-radius: 10px;
  }
  
  .article-thumbnail {
    width: 100%;
    height: 200px;
    object-fit: cover;
    margin-bottom: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1);
  }
  
  .article-content {
    flex-grow: 1;
  }
  
  .article-title {
    font-size: 1.5em;
    margin: 0 0 10px 0;
    color: #333;
  }
  
  .article-date {
    color: #888;
    font-weight: 600;
    margin-bottom: 10px;
  }
  
  .article-summary {
    color: #555;
  }
  
  /* Responsive design for smaller screens */
  @media (max-width: 768px) {
    .articles {
      flex-direction: column;
    }
  
    .article-item {
      flex: 1 1 100%;
    }
  }
  </style>
  