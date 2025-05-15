<script setup>
import logo from "../../assets/logo.png";
import Button from "../Slots/Button.vue";
import { ref } from "vue";
const links = ref([
  { name: "Home", href: "#home" },
  { name: "Services", href: "#services" },
  { name: "Projects", href: "#projects" },
  { name: "FAQs", href: "#faqs" },
  { name: "About us", href: "#about" },
]);
</script>

<template>
  <div class="navigation-wrapper">
    <nav class="navigation">
      <ul>
        <li>
          <p><span>Med</span><span class="envision">Envision</span></p>
        </li>
        <li v-for="link in links" :key="link.name">
          <a :href="link.href">{{ link.name }}</a>
        </li>
        <li>
          <Button
            backgroundColor="#198ae3"
            text="Request Quote"
            color="#fff"
            size="large"
            :isArrow="false"
          />
        </li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
.navigation-wrapper {
  padding-top: 50px;
  width: 60%;
  margin: 0 auto;
}

.navigation {
  font-family: Arial, Helvetica, sans-serif;
  border: 1px solid white;
  border-radius: 100px;
  background: white;
  padding: 15px 0;
}

ul {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 30px;
}

li a {
  color: black;
  font-size: 13px;
}

p,
span {
  color: black;
  font-size: 20px;
  font-weight: bold;
}

span {
  color: #198ae3;
}

.envision {
  color: black;
}

button {
  background: #198ae3;
  border: none;
  border-radius: 100px;
  padding: 10px 20px;
  font-size: 14px;
  color: white;
  cursor: pointer;
}
</style>
