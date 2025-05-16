<script setup>
import Title from "../Slots/Title.vue";
import Button from "../Slots/Button.vue";
</script>

<template>
  <main class="main">
    <div class="showcase">
      <div class="showcase-list">
        <Title>
          <template #title>MedEnvision Features</template>
        </Title>
        <div class="showcase-item">
          <h2 class="first-title">Make the future possible</h2>
          <p>
            MedEnvision is a leading provider of innovative technology solutions
            for the healthcare industry. Our mission is to empower healthcare
            professionals with cutting-edge tools and resources that enhance
            patient care, streamline operations, and drive better outcomes.
          </p>
        </div>
        <div class="showcase-item">
          <h2 class="first-title">Help Expand and Develop</h2>
          <p>
            MedEnvision is a leading provider of innovative technology solutions
            for the healthcare industry. Our mission is to empower healthcare
            professionals with cutting-edge.
          </p>
        </div>
        <div class="showcase-item">
          <h2 class="first-title">We Save more Lives</h2>
          <p>
            MedEnvision is a leading provider of innovative technology solutions
            for the healthcare industry. Our mission is to empower healthcare
            professionals with cutting-edge.
          </p>
        </div>

        <Button
          class="showcase-button"
          backgroundColor="#fff"
          text="Contact us"
          color="#000"
          size="large"
          border="1px solid black"
          :isArrow="true"
        />
      </div>
      <div class="showcase-image">
        <div class="card">
          <div class="mini-background">
            <i class="fas fa-play video-icon"></i>

            <!-- Video Icon -->
          </div>
          <h1>Discover More What We Do</h1>
          <p>Renovation . Installation</p>
          <Button
            class="button"
            text="Get Involved"
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
  background-image: url("/src/assets/feature.jpg");
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
  background-image: url("/src/assets/bg.jpg");
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
</style>
