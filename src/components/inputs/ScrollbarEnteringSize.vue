<script setup lang="ts"></script>

<template>
  <input type="text" placeholder="8px" class="input"></input>
</template>

<style lang="scss">
.input {
  color: rgba(255, 255, 255, 0.78);
  font-weight: 400;
  font-size: 14px;
  left: 0px;
  border: none;
  width: 100%;
  background: none;
  place-content: inherit;

  &:focus {
    outline: none;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
</style>
