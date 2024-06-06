<script setup lang="ts">

const props = defineProps({
  innerText: {
    type: String,
    default: "inner-Text",
    required: true,
  },
  colorText: {
    type: String,
    default: "black",
    required: true,
  },
  backgroundColor: {
    type: String,
    default: "none",
    required: true,
  },
  foo: {
    type: Function,
  },
});
</script>

<template>
  <button
    v-on:click="props.foo"
    class="wrapperButton"
    :style="{ color: colorText, background: backgroundColor }"
  >
    {{ innerText }}
  </button>

</template>

<style lang="scss">
.wrapperButton {
  position: relative;
  font-family: "Inter", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;

  display: flex;
  flex-direction: row;
  justify-content: center;
  align-self: center;

  text-transform: uppercase;

  padding: 6px 7px;
  margin: 0 10px;

  border: none;

  border-radius: 3px;
  color: black;

  &:first-child {
    margin-left: 0px !important;
  }

  &:last-child {
    margin-right: 0px !important;
  }

  &:active {
    font-weight: 600;
  }

  &:focus {
    font-weight: 600;
    &::before {
      content: "";
      position: absolute;

      width: 80%;
      height: 3px;
      border-radius: 2px;
      background-color: white;

      bottom: 0px;
    }
  }

  cursor: pointer;
}
</style>
