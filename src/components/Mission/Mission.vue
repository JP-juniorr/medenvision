<script setup>
import Title from "../Slots/Title.vue";
import Button from "../Slots/Button.vue";
</script>
<template>
  <div class="main">
    <Title>
      <template #title>Our Mission</template>
    </Title>
    <div>
      <h2>
        Our mission is to revolutionize the world of technology by providing
        innovative solutions that enhance the quality of life for individuals
        and communities. We strive to create a sustainable future through
        cutting-edge technology, exceptional service, and a commitment to
        excellence.
      </h2>
      <div class="cards">
        <div class="cards_1">
          <i class="fa-solid fa-plus"></i>
          <h2>Mission</h2>
          <p>
            Our mission is to revolutionize the world of technology by providing
            innovative solutions that enhance the quality of life for
            individuals and communities. We strive to create a sustainable
          </p>
          <Button
            class="showcase-button"
            backgroundColor="#fff"
            text="Expand Mission"
            color="#000"
            size="large"
            :isArrow="true"
          />
        </div>
        <div class="cards_2">
          <i class="fa-solid fa-plus"></i>
          <h2>Vision</h2>
          <p>
            Our vision is to be a global leader in technology solutions,
            recognized for our commitment to innovation, quality, and customer
            satisfaction. We aim to empower individuals and organizations to
            achieve their goals through the use of advanced technology.
          </p>
          <Button
            class="showcase-button"
            backgroundColor="#fff"
            text="Expand Vision"
            color="#000"
            size="large"
            :isArrow="true"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<style scope>
.main {
  font-family: "Courier New", Courier, monospace;
  background-color: #f6f9fe;
  width: 100%;
  margin: 0px auto;
  padding: 20px;
}
h2 {
  font-size: 16px;
  color: #333;
  margin-top: 10px;
}
p {
  font-size: 14px;
  color: #555;
  margin-top: 10px;
}
.cards {
  width: 100%;
  display: flex;
  flex-direction: row;
  margin-top: 20px;

  height: 30vh;
}
.cards_1 {
  border: 1px solid #353333;
  height: 100%;
  width: 100%;
  margin-right: 50px;
  background: white;
}
.cards_2 {
  border: 1px solid #353333;
  height: 100%;
  width: 100%;
  background: white;
}
.cards_1,
.cards_2 {
  padding: 30px;
}
.cards i {
  background: black;
  color: white;
  padding: 15px;
}
.showcase-button {
  margin-top: 20px;
}
</style>
