<script setup>
import { ref } from "vue";
import Button from "../Slots/Button.vue";
const props = defineProps({
  text: {
    type: String,
    default: "Button",
  },
  source: {
    type: String,
    default: "https://via.placeholder.com/150",
  },
  backgroundColor: {
    type: String,
    default: "#fff",
  },
  width: {
    type: String,
    default: "100px",
  },
  height: {
    type: String,
    default: "100px",
  },
  button: {
    type: String,
    default: "Click Me",
  },
});
</script>
<template>
  <div :style="{ backgroundColor: backgroundColor }" class="main">
    <div class="logo-part">
      <slot name="logo">
        <img
          :style="{ width: width, height: height }"
          :src="source"
          alt="Logo"
        />
      </slot>
    </div>
    <div class="text-part">
      <slot name="text">
        <p>
          {{ text }}
        </p>
      </slot>
    </div>
    <div class="button-part">
      <slot name="button">
        <Button color="black" :isArrow="true" class="button" :text="button" />
      </slot>
    </div>
  </div>
</template>
<style scoped>
.main {
  border: 1px solid black;
  width: 100%;
  height: 100%;
  position: relative;
}
.main p {
  margin-bottom: 30px;
}
.button {
  margin-top: 10px;
  position: absolute;
  bottom: 0px;
  right: 0px;
}
</style>
