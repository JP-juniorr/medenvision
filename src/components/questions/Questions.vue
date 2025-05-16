<script setup>
import Title from "../Slots/Title.vue";
import Button from "../Slots/Button.vue";

import { ref } from "vue";

// Array of FAQs
const faqs = ref([
  {
    question: "What types of medical equipment do you install?",
    answer:
      "We install a wide range of medical equipment, including diagnostic machines, surgical tools, and patient monitoring systems.",
  },
  {
    question: "Do you provide custom interior design solutions?",
    answer:
      "Yes, we tailor each design to the specific needs of the healthcare facility, focusing on both aesthetics and functionality.",
  },
  {
    question: "Can you handle large-scale hospital projects?",
    answer:
      "Yes, we have the expertise and resources to manage large-scale hospital projects efficiently.",
  },
  {
    question: "How long does a project typically take?",
    answer:
      "Project duration varies depending on scope, but typically ranges from 3 to 12 months.",
  },
  {
    question: "What is your warranty policy?",
    answer:
      "We offer a comprehensive warranty on all installations, covering both equipment and workmanship.",
  },
  {
    question: "Do you provide training for hospital staff?",
    answer:
      "Yes, we offer training sessions for hospital staff to ensure they are comfortable using the new equipment.",
  },
  {
    question: "How do you ensure compliance with healthcare regulations?",
    answer:
      "We stay updated on all healthcare regulations and ensure that our installations meet or exceed these standards.",
  },
  {
    question: "What is your approach to project management?",
    answer:
      "We use a structured project management approach, including regular updates and milestones, to ensure timely completion.",
  },
]);

// Track the open/closed state of each FAQ
const openIndices = ref([]);
const toggleFAQ = (index) => {
  const currentIndex = openIndices.value.indexOf(index);
  if (currentIndex === -1) {
    openIndices.value.push(index);
  } else {
    openIndices.value.splice(currentIndex, 1);
  }
};
</script>

<template>
  <main class="main">
    <div class="showcase">
      <div class="showcase-list">
        <h1>Asked Questions</h1>
        <div class="faq-container">
          <div class="faq-list">
            <div v-for="(faq, index) in faqs" :key="index" class="faq-item">
              <div class="question" @click="toggleFAQ(index)">
                {{ faq.question }}
                <span class="toggle-icon">{{
                  openIndices.includes(index) ? "−" : "+"
                }}</span>
              </div>
              <div v-if="openIndices.includes(index)" class="answer">
                {{ faq.answer }}
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="showcase-image">
        <div class="card">
          <div class="mini-background">
            <i class="fas fa-play video-icon"></i>

            <!-- Video Icon -->
          </div>
          <h1>Contact us</h1>
          <p>info@MedEnvision.com.ck</p>
          <Button
            class="button"
            text="Talk to us"
            color="black"
            backgroundColor="transparent"
            borderRadius="5px"
            padding="10px 20px"
            fontSize="16px"
            :isArrow="true"
          />
        </div>
      </div>
    </div>
  </main>
</template>
<style scoped>
.main {
  font-family: "Courier New", Courier, monospace;
  background-color: #fff;
  width: 100%;
  margin: 0px auto;
}
.showcase {
  display: flex;
  justify-content: space-between;
}
.showcase-list {
  width: 50%;
  padding: 20px;
}
.shoecase-list h2 {
  margin: 20px 0px;
  font-size: 2rem;
  color: #000;
}
.showcase-list p {
  font-size: 1rem;
  margin: 10px 0px;
  color: #000;
}
.showcase-image {
  width: 100%;
  height: 100vh;
  background-image: url("/src/assets/hospital.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  position: relative;
}
.first-title {
  font-size: 2rem;
  margin: 20px 0px;
  color: #000;
  width: 70%;
}
.showcase-button {
  margin-top: 50px;
}

.mini-background {
  width: 100%;
  height: 15vh;
  background-image: url("/src/assets/hospital2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.card {
  position: absolute;
  top: 80%;
  right: -13%;
  transform: translate(-50%, -50%);
  background-color: rgba(255, 255, 255);
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
}

.card h1 {
  font-family: "Courier New", Courier, monospace;
  font-size: 1.8em;
  margin-bottom: 10px;
  padding-top: 15px;
}
.card p {
  font-family: "Courier New", Courier, monospace;
  font-size: 1.2em;
  margin-bottom: 5px;
}
.button {
  margin-left: -20px;
}
.video-icon {
  font-size: 24px;
  color: #fff;
  margin-top: 10px;
}

.faq-container {
  font-family: "Arial", sans-serif;
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
}

h2 {
  font-size: 24px;
  color: #1e1e2f;
  margin-bottom: 20px;
  text-align: left;
}

.faq-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.faq-item {
  border-bottom: 1px solid #e0e0e0;
  padding-bottom: 10px;
}

.question {
  font-family: "Courier New", Courier, monospace;
  font-size: 16px;
  color: #333;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
}

.toggle-icon {
  font-size: 18px;
  color: black;
  transition: transform 0.2s;
}

.answer {
  font-size: 14px;
  color: #fff;
  background-color: black;
  padding: 15px;
  border-radius: 5px;
  margin-top: 10px;
  line-height: 1.5;
}
</style>
