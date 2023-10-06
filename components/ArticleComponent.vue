<template>
    <div @click="goToDetail(id)">
        <h1>this is component the heading</h1>

        <p>this is the component body</p>
        <p> title: {{ title }} by {{ author }}</p>
    </div>
</template>

<script setup>
import { useRoute } from 'vue-router';

defineProps({
    id: String,
    title: String,
    author: String
})

import { useRouter } from 'vue-router'

const { push } = useRouter();

const goToDetail = (pictureId) => {
  push(`/pictures/${pictureId}`);
};

</script>