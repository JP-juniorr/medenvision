<script setup>
import { ref } from "vue";
import Title from "../Slots/Title.vue";
import Cards from "../Slots/Cards.vue";

// Define the logos dynamically
const logos = ref([
  {
    src: new URL("../../assets/logos/logo1.png", import.meta.url).href,
    text: "Innovating the future of transportation technology solutions for a better tomorrow.",
  },
  {
    src: new URL("../../assets/logos/logo2.png", import.meta.url).href,
    text: "Trusted by industry leaders worldwide for quality and reliability in sport technology.",
  },
  {
    src: new URL("../../assets/logos/logo3.png", import.meta.url).href,
    text: "Delivering excellence in every project for over 20 years in the field of sport technology.",
  },
  {
    src: new URL("../../assets/logos/logo4.png", import.meta.url).href,
    text: "Revolutionizing transportation technology with cutting-edge solutions for a sustainable future in transportation.",
  },
  {
    src: new URL("../../assets/logos/logo5.png", import.meta.url).href,
    text: "Building a healthier tomorrow with innovative solutions in delivery technology for a better world.",
  },
  {
    src: new URL("../../assets/logos/logo8.png", import.meta.url).href,
    text: "Building a healthier tomorrow with innovative solutions in gaming technology for a better world and a brighter future.",
  },
  {
    src: new URL("../../assets/logos/logo11.png", import.meta.url).href,
    text: "Building a healthier tomorrow with innovative solutions in gaming technology for a better world and a brighter future.",
  },
]);
</script>

<template>
  <div class="main">
    <div class="partners">
      <!-- Title Component -->
      <div class="partners-title">
        <Title>
          <template #title>Our Partners</template>
        </Title>
      </div>

      <!-- Dynamically Render Cards -->
      <div class="partners-list">
        <Cards
          v-for="(logo, index) in logos"
          :key="index"
          :text="logo.text"
          :source="logo.src"
          backgroundColor="#fff"
          width="150px"
          height="150px"
          button="Discover More"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.main {
  font-family: "Courier New", Courier, monospace;
  background-color: #f6f9fe;
  width: 100%;
  margin: 10px auto;
  padding: 20px;
}

.partners-list {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(4, 1fr); /* Responsive grid */
  gap: 20px;
}

.partners-title {
  margin-bottom: 20px;
  text-align: center;
}
</style>
