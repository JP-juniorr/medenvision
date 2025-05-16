<script setup>
import NavigationVue from "../Navigation/Navigation.vue";
import Button from "../Slots/Button.vue";
import Title from "../Slots/Title.vue";
</script>
<template>
  <div class="showcase">
    <NavigationVue />
    <h1>
      <span>Redefining Healthcare </span> <br />
      with Technology and Design
    </h1>
    <p>
      From cutting-edge medical equipment instalttions to thoughtfully designed
      interiors, <br />
      we create functional, patient-friendly environments that sets new
      standards.
    </p>
    <p>
      Our team of experts is dedicated to delivering innovative solutions that
      enhance the quality of care and improve patient outcomes.
      <br />
      We are committed to providing the highest level of service and support to
      our clients, ensuring that every project is a success.
    </p>
    <div class="buttons">
      <Button
        backgroundColor="#fff"
        text="Contact us"
        color="#000"
        size="large"
        border="1px solid black"
        :isArrow="true"
      />
    </div>
  </div>
</template>

<style scoped>
.showcase {
  background-color: #f6f9fe;
  height: 80vh;
}
h1 {
  font-family: "Courier New", Courier, monospace;
  font-size: 50px;
  color: #00041f;
  text-align: center;
  margin-top: 100px;
  line-height: 60px;
}
span {
  color: #00041f;
}
p {
  font-family: "Poppins", sans-serif;
  font-size: 18px;
  font-weight: lighter;
  color: #454343;
  text-align: center;
  margin-top: 20px;
  line-height: 30px;
}
div {
  text-align: center;
}
.buttons {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
}
.buttons .left {
  margin-right: 20px;
}
</style>
