<script setup>
import BackgroundImage from "../../assets/bg.jpg";
import Button from "../../components/Slots/Button.vue";
import bg2 from "../../assets/bg2.jpg";
</script>

<template>
  <div class="background">
    <div class="card">
      <div class="mini-background">
        <i class="fas fa-play video-icon"></i>

        <!-- Video Icon -->
      </div>
      <h1>NINCOME INFRASTRUCTURE</h1>
      <p>Renovation . Installation</p>
      <Button
        class="button"
        text="Get Started"
        color="black"
        backgroundColor="transparent"
        borderRadius="5px"
        padding="10px 20px"
        fontSize="16px"
        :isArrow="true"
      />
    </div>
  </div>
</template>

<style scoped>
.background {
  position: relative;
  width: 100%;
  height: 80vh;
  background-image: url("/src/assets/bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
.mini-background {
  width: 100%;
  height: 15vh;
  background-image: url("/src/assets/bg2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.mini-background i {
  font-size: 50px;
  color: #fff;
  margin-top: 10px;
  font-weight: 200px;
}
.card {
  position: absolute;
  top: 70%;
  right: -10%;
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
