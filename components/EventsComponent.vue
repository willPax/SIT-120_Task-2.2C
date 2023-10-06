
<script setup>
import { ref } from 'vue';

const upcomingEvents = ref([
  {
    id: 1,
    title: "Ancient Artifacts Exhibition",
    date: "2024-03-15",
    description: "Discover artifacts from ancient civilizations...",
    image: '../src/assets/images/eventpik4.jpg'
  },
]);


const pastEvents = ref([
    {id: 1,
    title: "Renaissance Revelry",
    date: "2023-01-15",
    description: "A throwback to the art and culture of the Renaissance era...",
    image: '../src/assets/images/eventpik1.jpg'},
    {id: 2,
    title: "Renaissance Revelry",
    date: "2023-01-15",
    description: "A throwback to the art and culture of the Renaissance era...",
    image: '../src/assets/images/eventpik2.jpg'},
    {id: 3,
    title: "Renaissance Revelry",
    date: "2023-01-15",
    description: "A throwback to the art and culture of the Renaissance era...",
    image: '../src/assets/images/eventpik3.jpg'},
    ]);
</script>

<template>
    
  <div class="main-container">   
    <div class="alternate-container">
        <h1>Upcoming Events</h1>
        <div class="event" v-for="event in upcomingEvents" :key="event.id">
            <img :src="event.image" alt="Past Event Image" class="event-image">
            <h2>{{ event.title }}</h2>
            <p>Date: {{ event.date }}</p>
            <p>{{ event.description }}</p>
        </div>
    </div>
    <div class="alternate-container">
        <h1>Past Events</h1>
        <div class="past-event">
            <div class="event" v-for="event in pastEvents" :key="event.id">
                <img :src="event.image" alt="Past Event Image" class="event-image">
                <h2>{{ event.title }}</h2>
                <p>Date: {{ event.date }}</p>
                <p>{{ event.description }}</p>
            </div>
        </div>
    </div>
  </div>
</template>

<style scoped>


.event-image {
    width: 100%;
    height: 400px;
    object-fit: cover;
    margin-bottom: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1);
}

.past-event {
    /* display: flex; */
    gap: 20px;
    align-items: center;
    margin-bottom: 40px;
}
</style>