<script setup lang="ts">
import { ref } from "vue";

const props = defineProps({
  defaultSize: {
    type: Number,
    required: true,
  },
});

const checkingForNumber = (value: Number | String) => {
  console.log(value);
  if (typeof(value) !== "number") {
    console.log("this not number");
    return "";
  }
  return value;
};

const valueSize = ref(checkingForNumber(props.defaultSize) + "px");
console.log(valueSize.value, "valueSize");
</script>

<template>
  <input
    type="text"
    class="input"
    placeholder="8 px"
    v-model="valueSize"
    @change="checkingForNumber($event.target?.value)"
  />
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
