
<script setup>

import { ref } from 'vue';

const isMenuOpen = ref(false);

function closeMenu(){
  isMenuOpen.value = false;
}
</script>
<template>
  <div class="nav-container">
      <input type="checkbox" id="menu-toggle" class="menu-toggle" v-model="isMenuOpen" />
      <label for="menu-toggle" class="dropdown-btn">Menu</label>
      <div class="links-container">
          <RouterLink class="nav-link" to="/" @click="closeMenu">Home</RouterLink>
          <RouterLink class="nav-link" to="/about" @click="closeMenu">About</RouterLink>
          <RouterLink class="nav-link" to="/articles" @click="closeMenu">Articles</RouterLink>
          <RouterLink class="nav-link" to="/pictures" @click="closeMenu">Pictures</RouterLink>
          <RouterLink class="nav-link" to="/contact" @click="closeMenu">Contact</RouterLink>
          <RouterLink class="nav-link" to="/events" @click="closeMenu">Events</RouterLink>
      </div>
  </div>
</template>


<style scoped>

.nav-container, .nav-link, .dropdown-btn {
font-family: 'Arial', sans-serif;
}

.nav-container {
display: flex;
justify-content: center;
background-color: #ffffff; /* Matches article's background for consistency */
padding: 10px 20px; /* Increased padding for a more modern look */
position: relative;
border-bottom: 1px solid #eee; /* Light border to separate from content */
flex-wrap: wrap;
}

.nav-link {
text-decoration: none;
color: #555; /* Slightly darker for better contrast */
padding: 10px 20px;
margin: 0 10px;
font-size: 1.1em;
transition: background-color 0.3s, color 0.3s;
border-radius: 4px;
}

.nav-link:hover {
background-color: #f7f7f7; /* Light gray for hover */
color: #333; /* Slightly darker color for hover */
}

.router-link-active {
color: #333;
background-color: #ecf0f1; /* Neutral highlight */
border-radius: 4px;
}

.router-link-active:hover {
background-color: #d7dadc; /* A shade darker for hover on active link */
color: #333;
}

/* Mobile styles */
.menu-toggle {
display: none; 
}

.dropdown-btn {
display: none;
background-color: #f7f7f7; /* Light gray to match overall theme */
color: #555;
padding: 10px 20px;
border: 1px solid #eee;
cursor: pointer;
border-radius: 4px;
}

.links-container {
display: flex;
}

/* Media query for small screens */
@media (max-width: 768px) {
.nav-container{
    justify-content: space-between; /* For better layout on mobile */
}

.dropdown-btn {
  display: block;
}

.links-container {
  display: none;
  flex-direction: column;
  position: absolute;
  top: 100%;
  left: 0;
  right: 0;
  background-color: #ffffff; /* Same as navbar */
  box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.1); /* Soft shadow for depth */
  border-radius: 0 0 5px 5px; /* Rounded corners for bottom part */
  z-index: 1; /* Ensure it overlays content below */
}

.menu-toggle:checked + .dropdown-btn + .links-container {
  display: flex; 
}
}

</style>
