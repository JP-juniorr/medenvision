<script setup>
import { ref } from "vue";
import Title from "../../components/Slots/Title.vue";
</script>

<template>
  <div class="main">
    <Title>
      <template #title>Who are we</template>
    </Title>
    <div class="partners">
      <p>
        We are a team of passionate individuals dedicated to creating innovative
        solutions that make a difference. Our mission is to leverage technology
        to improve lives and drive progress in various industries. With a focus
        on quality, reliability, and customer satisfaction, we strive to exceed
        expectations and deliver exceptional results.
      </p>
      <p>
        Our team consists of experts in various fields, including software
        development, design, and project management. We work collaboratively to
        ensure that every project is executed with precision and care. Our
        commitment to continuous improvement drives us to stay ahead of the
        curve and embrace new challenges with enthusiasm.
      </p>
      <p>
        We believe in the power of technology to transform lives and create a
        better future. Our vision is to be a leader in our industry, known for
        our innovative solutions and exceptional service. We are excited about
        the future and look forward to making a positive impact on the world.
      </p>
      <p>
        Join us on our journey as we continue to push the boundaries of what is
        possible and strive for excellence in everything we do.
      </p>
      <p>
        We are committed to building strong partnerships with our clients and
        stakeholders, working together to achieve common goals and drive
        success. Our collaborative approach ensures that we understand your
        needs and deliver solutions that meet your unique requirements.
      </p>
    </div>
  </div>
</template>

<style scoped>
.main {
  font-family: "Courier New", Courier, monospace;
  background-color: #f6f9fe;
  width: 100%;
  margin: 0px auto;
  padding: 20px;
}
.partners {
  display: flex;
  flex-direction: column;
  align-items: left;
  justify-content: left;
  margin-top: 20px;
}
.partners p {
  margin: 10px 0;
  background: white;
  border: 1px solid black;
  padding: 20px;
  line-height: 1.6;
}
</style>
