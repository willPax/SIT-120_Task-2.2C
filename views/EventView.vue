<template>
    <div class="main-heading">
        <h1>See our upcoming events</h1>
        <p>or brows over passed events you missed out on, and regret not turning up</p>
    </div>

    <EventsComponent/>
</template>


<script setup>
import EventsComponent from '../components/EventsComponent.vue';
import { ref } from 'vue';

const upcomingEvents = ref([
  {
    id: 1,
    title: "Ancient Artifacts Exhibition",
    date: "2024-03-15",
    description: "Discover artifacts from ancient civilizations..."
  },
  // ... other events
]);

const pastEventImage = 'path_to_past_event_image.jpg';
const pastEvent = {
  title: "Renaissance Revelry",
  date: "2023-01-15",
  description: "A throwback to the art and culture of the Renaissance era..."
};
</script>

<style scoped>
.events-container {
    font-family: 'Roboto', sans-serif;
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
}

h1 {
    font-size: 2.2em;
    color: #2C3A47;
    margin-bottom: 30px;
}

h2 {
    font-size: 1.8em;
    margin-bottom: 20px;
    color: #34495e;
}

.event-image {
    max-width: 100%;
    height: auto;
    margin-right: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.past-event {
    display: flex;
    gap: 20px;
    align-items: center;
    margin-bottom: 40px;
}
</style>

