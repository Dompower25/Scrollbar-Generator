<script setup lang="ts"></script>

<template>
  <div class="wrapper">
    <div class="scrollbar_style_block"></div>
    <div class="line"></div>
    <div class="css_style_block"></div>
  </div>
</template>

<style lang="scss">
@import "../styles/index.scss";

.wrapper {
  width: 70%;
  height: 500px;

  display: flex;
  justify-content: space-between;

  .line {
    width: 1px;
    height: 100%;
    border: none;
    background: #ffffff33;
    margin: auto 62px;
  }

  .scrollbar_style_block {
    width: 100%;
    height: 100%;

    border: 1px solid white;
  }
  .css_style_block {
    width: 100%;
    height: 100%;

    border: 1px solid yellow;
  }
}
</style>
