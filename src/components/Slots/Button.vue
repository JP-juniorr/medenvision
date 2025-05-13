<script setup>
const props = defineProps({
  text: {
    type: String,
    default: "Button",
  },
  backgroundColor: {
    type: String,
    default: "#fff",
  },
  color: {
    type: String,
    default: "#198ae3",
  },
  size: {
    type: String,
    default: "medium",
  },
  border: {
    type: String,
    default: "none",
  },
  isArrow: {
    type: Boolean,
    default: false,
  },
});
</script>
<template>
  <button
    class="custom-button"
    :style="{ backgroundColor: backgroundColor, border: border, color: color }"
  >
    <slot>{{ text }}</slot>
    <span v-if="isArrow" class="arrow">→</span>
  </button>
</template>

<style scoped>
.custom-button {
  border: none;
  border-radius: 100px;
  padding: 10px 20px;
  font-size: 14px;
  cursor: pointer;
  display: flex;
  align-items: center;
  font-family: Arial, Helvetica, sans-serif;
}

.arrow {
  font-size: 14px;
  margin-left: 10px;
}
</style>
