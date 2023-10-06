<script setup>
defineProps({
    image: String,
    id: Number

})

function getImage(title){
    const url = '../assets/images/pik'+title+'.jpg'
    return new URL(url, import.meta.url).href
}

function goToDetail(pictureId) {
      this.$router.push(`/pictures/${pictureId}`);
    }

</script>

<template>
        <!-- <p>heres the image: {{ image.title }} </p> -->

<p></p>
        <div class="image-view">
            <img :src=getImage(image.id) :alt="alt" @error="handleError" @click="goToDetail(image.id)"/>
                <div class="floating-text" v-if="!error">{{ image.title }}</div>
                <div v-if="error" class="error-message">Failed to load image</div>
         </div>


</template>

<style scoped>


.image-view {
  position: relative;
  max-width: 500px;
}

.image-view img {
  max-width: 100%;
  display: block;
  border-radius: 5px;
}
.floating-text {
  position: absolute;
  bottom: 15px; /* You can adjust this to place the text where you prefer */
  left: 15px; /* Adjusting this as well for positioning */
  color: white;
  background-color: rgba(0, 0, 0, 0.6);
  padding: 10px 15px;
  border-radius: 5px;
}
</style>