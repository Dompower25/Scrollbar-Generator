<script setup lang="ts">
import Wrapper from "./components/Wrapper.vue";
</script>

<template>
  <div class="template">
    <div class="main_title">css scroll visual constructor</div>
    <Wrapper />

  </div>
  
</template>

<style lang="scss">
@import "./styles/index.scss";

.template {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.main_title {
  color: $mainTextColor;
  font-size: 32px;
  font-weight: 600;
  line-height: 38.73px;
  text-transform: uppercase;
  margin-bottom: 70px;
}
</style>
