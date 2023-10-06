<template>
    <div class="image-view">
      <img :src="src" :alt="alt" @error="handleError" />
      <div v-if="error" class="error-message">Failed to load image</div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      src: {
        type: String,
        required: true,
      },
      alt: {
        type: String,
        default: '',
      },
    },
    data() {
      return {
        error: false,
      };
    },
    methods: {
      handleError() {
        this.error = true;
      },
    },
  };
  </script>
  
  <style scoped>
  .image-view {
    position: relative;
    max-width: 100%;
    border: 1px solid #ddd;
  }
  
  .image-view img {
    max-width: 100%;
    display: block;
    border-radius: 5px;
  }
  
  .error-message {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: red;
    font-weight: bold;
  }
  </style>
  