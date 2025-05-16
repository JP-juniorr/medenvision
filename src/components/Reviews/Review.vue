<script setup>
import Title from "../Slots/Title.vue";
import img from "../../assets/reviewsicon.png";
import img2 from "../../assets/pic2.png";
import img3 from "../../assets/pic3.jpg";
import Button from "../Slots/Button.vue";
import { ref } from "vue";

// Array of testimonials
const testimonials = ref([
  {
    name: "Dr. Patel",
    title: "Diagnostic Lab Owner",
    image: img, // Placeholder image
    review:
      "The team at this clinic has transformed our diagnostic lab with their state-of-the-art technology. The installation was seamless, and the results have been outstanding.",
  },
  {
    name: "Sarah Johnson",
    title: "Pediatrician",
    image: img2,
    review:
      "I can't thank this clinic enough for their exceptional service. The technology they provided has made a significant difference in our practice, and the interior design is simply beautiful.",
  },
  {
    name: "Michael Lee",
    title: "Clinic Manager",
    image: img3,
    review:
      "Working with this clinic has been a game-changer for us. Their attention to detail in both technology installation and interior design is unmatched. Our clinic feels like a brand-new space!",
  },
]);

// Track the current testimonial index
const currentIndex = ref(0);

// Navigate to the previous testimonial
const prevTestimonial = () => {
  currentIndex.value =
    (currentIndex.value - 1 + testimonials.value.length) %
    testimonials.value.length;
};

// Navigate to the next testimonial
const nextTestimonial = () => {
  currentIndex.value = (currentIndex.value + 1) % testimonials.value.length;
};
</script>
<template>
  <div class="review">
    <div class="review-title">
      <Title>
        <template #title>Testimonials</template>
      </Title>
    </div>
    <div class="review-list">
      <div class="review-text">
        <p>
          Precision and care. Their attention to detail in both technology
          installation and interior design is unmatched. Our clinic feels like a
          brand-new space! The equipment is top-notch, and the interior design
          has created a welcoming and professional atmosphere for patients.
          <br />
          precision and care. Their attention to detail in both technology
          installation and interior design is unmatched. Our clinic feels like a
          brand-new space! The equipment is top-notch, and the interior design
          has created a welcoming and professional atmosphere for patients.
        </p>
      </div>

      <div class="testimonials">
        <!-- Testimonial content -->
        <div class="testimonial-item">
          <img
            :src="testimonials[currentIndex].image"
            alt="Profile"
            class="profile-pic"
          />
          <p class="name">
            {{ testimonials[currentIndex].name }},
            {{ testimonials[currentIndex].title }}
          </p>
          <p class="opinion">
            {{ testimonials[currentIndex].review }}
          </p>
        </div>
        <!-- Navigation arrows -->
        <div class="arrows">
          <button @click="prevTestimonial" class="arrow left-arrow">
            &larr;
          </button>
          <button @click="nextTestimonial" class="arrow right-arrow">
            &rarr;
          </button>
          <Button
            class="showcase-button"
            backgroundColor="#fff"
            text="Check all reviews"
            color="#000"
            size="large"
            border="none"
            :isArrow="true"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.review {
  display: flex;
  flex-direction: column;
  align-items: left;
  justify-content: center;
  font-family: "Courier New", Courier, monospace;
  height: 50vh;
  padding: 20px;
  background: #f6f9fe;
}
.review-title {
  margin-top: 20px;
}
.review-list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  padding-top: 70px;
}
.review-text p {
  width: 80%;
  display: flex;
  flex-wrap: wrap;
  border-radius: 10px;
}

.testimonials {
  background-color: #fff;
  padding: 20px;
}
.testimonials p {
  font-family: "Courier New", Courier, monospace;
  font-size: 16px;
  color: #333;
  margin: 0;
  padding: 10px;
}
.testimonials img {
  border-radius: 50%;
  width: 50px;
  height: 50px;
}

.testimonial-item {
  display: flex;
  flex-direction: column;
  gap: 15px;
}
.testimonial-item img {
  border-radius: 50%;
  width: 50px;
  height: 50px;
}

.testimonial-item p {
  font-family: "Courier New", Courier, monospace;
  font-size: 16px;
  color: #333;
  margin: 0;
  padding: 0px !important;
}

.profile-pic {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  object-fit: cover;
}

.name {
  font-family: "Arial", sans-serif;
  font-size: 16px;
  font-weight: bold;
  color: #333;
  margin: 0;
}

.arrows {
  display: flex;
  gap: 10px;
  margin-top: 10px;
  position: relative;
}

.arrow {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  border: none;
  background-color: #e0e0e0;
  color: #333;
  font-size: 16px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background-color 0.3s;
}

.right-arrow {
  background-color: #198ae3;
  color: white;
}

.arrow:hover {
  background-color: #ccc;
}

.right-arrow:hover {
  background-color: #156bb5;
}

.showcase-button {
  position: absolute;
  right: -10px;
  bottom: -15px;
  margin-top: 20px;
}
</style>
