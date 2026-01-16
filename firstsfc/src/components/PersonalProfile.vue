<template>
  <div id="app">
    <header>
      <h1>{{ name }}</h1>
      <p>Welcome to my personal profile page!</p>
    </header>

    <nav class="navbar">
      <a href="#about" @click.prevent="scrollTo('#about')">About</a>
      <a href="#education" @click.prevent="scrollTo('#education')">Education</a>
      <a href="#goals" @click.prevent="scrollTo('#goals')">Goals</a>
      <a href="#gallery" @click.prevent="scrollTo('#gallery')">Gallery</a>
    </nav>

    <div class="container">
      <aside class="side" id="about">
        <h2>About Me</h2>
        <p>Hello Everyone! I love CATS 🐱</p>
        <img 
          src="https://www.animalia-life.club/data_images/cat/cat4.jpg" 
          alt="Cat" 
          class="profile-img"
        >
      </aside>

      <main class="main-content">
        <section id="education">
          <h2>Education / Achievements</h2>
          <p>Currently taking BSCS-SF in Asia Pacific College</p>
          <p>Experience: Coding Python</p>
        </section>

        <section id="hobbies">
          <h2>Hobbies</h2>
          <p>Cooking, Eating, Sleeping</p>
        </section>

        <section id="goals">
          <h2>Goals In Life</h2>
          <ul>
            <li v-for="(goal, index) in goals" :key="index">
              {{ goal }}
            </li>
          </ul>
        </section>

        <section id="gallery">
          <h2>Gallery</h2>
          <div class="gallery-grid">
            <img v-for="(img, index) in galleryImages" :key="index" :src="img" alt="Gallery item">
          </div>
        </section>
      </main>
    </div>

    <footer>
      <p>Contact: {{ email }} | © 2025 {{ name }}</p>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Data properties
const name = ref('Breneth Jian Ananayo');
const email = ref('bpananayo@student.apc.edu.ph');
const goals = ref([
  'Finish this course',
  'To own a Beluga Cat'
]);

const galleryImages = ref([
  'https://wallpapers.com/images/hd/ice-cream-pictures-93ucnuf5kr7ghmhg.jpg',
  'https://pallensmith.com/wp-content/uploads/CookingDemo.jpg',
  'https://cdn2.thecatapi.com/images/MTY3ODIyMQ.jpg'
]);

// Methods
const scrollTo = (selector) => {
  const element = document.querySelector(selector);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};
</script>

@import "./personalprofile.css";

<style scoped>
/* Scoped styles ensure they don't leak to other components */
.container {
  display: flex; /* Defaulting to Flexbox layout as per your comment */
  gap: 20px;
  padding: 20px;
}

.navbar {
  display: flex;
  gap: 15px;
  background: #333;
  padding: 1rem;
}

.navbar a {
  color: white;
  text-decoration: none;
}

.profile-img {
  width: 100%;
  max-width: 500px;
  height: auto;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 10px;
}

.gallery-grid img {
  width: 100%;
  border-radius: 8px;
}

footer {
  text-align: center;
  padding: 20px;
  margin-top: 40px;
  border-top: 1px solid #ccc;
}
</style>