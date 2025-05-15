<script setup>
const props = defineProps({
  title: {
    type: String,
    default: "Default Title",
  },
});
</script>

<template>
  <div class="title">
    <h1 class="title-text">
      <div class="title-container">
        <span class="arrow">
          <i class="fa-solid fa-caret-down"></i>
        </span>
        <slot name="title">{{ title }}</slot>
      </div>
    </h1>
  </div>
</template>

<style scoped>
.title {
  width: 100%;
  display: inline-flex;
  font-family: "Courier New", Courier, monospace;
}
.title-text h1 {
  display: inline-block !important;
  background: white;
}

.title-container {
  border: 1px solid #1e1e2f;
  display: inline-flex;
  align-items: center;
  background: white; /* White background for title and arrow */
  padding: 10px 20px;
  border-radius: 10px;
}

.title-text {
  font-size: 24px;
  font-weight: bold;
  color: #1e1e2f;
}

.arrow {
  margin-right: 10px;
  font-size: 24px;
  color: #1e1e2f;
}
</style>
