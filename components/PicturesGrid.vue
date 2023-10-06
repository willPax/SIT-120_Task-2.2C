<template>
  <div class="image-grid">
    <div v-for="(img, index) in images" :key="index" class="image-item" @click="goToDetail(img.id)">
      <img :src="img.src" :alt="img.alt" />
      <div class="floating-text">{{ img.index }} this is image title </div>
    </div>
  </div>
</template>

<script setup>
import { useRouter} from 'vue-router'
defineProps ({
  images: Array}
)

const { push } = useRouter();

const goToDetail = (pictureId) => {
  push(`/pictures/${pictureId}`);
};
</script>

<style scoped>
.image-grid {
  padding-top: 15px;
  column-count: 3;
  column-gap: 1em;
  width: 100%;
  transition: transform 0.3s;
}

.image-item {
  break-inside: avoid;
  margin-bottom: 1em;
  position: relative;
}

.image-item img {
  width: 100%;
  border-radius: 5px;
  transition: transform 0.3s;
}

.image-item img:hover{
  transform: scale(1.03);
} 

.floating-text {
  position: absolute;
  bottom: 10px;
  left: 10px;
  color: white;
  background-color: rgba(0, 0, 0, 0.7); /* semi-transparent black */
  padding: 5px 10px;
  border-radius: 5px;

  transition: transform 0.3s;
}
.image-grid div:hover {
  transform: scale(1.02);
}

</style>
