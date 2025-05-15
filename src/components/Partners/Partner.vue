<script setup>
import { ref } from "vue";
import Title from "../Slots/Title.vue";
import Cards from "../Slots/Cards.vue";

// Define the logos dynamically
const logos = ref(
  Array.from({ length: 5 }, (_, i) => ({
    src: new URL(`../../assets/logos/logo${i + 1}.png`, import.meta.url).href,
    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatibus.",
  }))
);
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
