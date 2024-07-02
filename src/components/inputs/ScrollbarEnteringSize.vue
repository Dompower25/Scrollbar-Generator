<script setup lang="ts">
import { ref } from "vue";

const props = defineProps({
  defaultSize: {
    type: Number,
    required: true,
  },
});

// требуется сделать backup версию значения инпута и если значение не изменилось вернуть прежнее значение.

// при взаимодействии с инспутом в виде клика на него, значение valueSize изменяется на ''

//  требуется добавить запрет на ввод значений не допустимых для данного вида инпута
//  например для установленном запретном типе данных в виде string -> в инпут нельзя вводить значение данного типа
//  при этом вывожить сообщение об неверном вводе либо каким-то другим образом показать юзеру о неверных действиях

const checkingForNumber = (value) => {
  console.log(value);

  if (typeof value) {
    console.log("is not number");
    return "change you is not number";
  }
  console.log("this number");
  return value;
};

const valueSize = ref(checkingForNumber(props.defaultSize));
console.log(valueSize.value)
</script>

<template>
  <input
    type="text"
    class="input"
    v-model="valueSize"
    @keyup="checkingForNumber($event.key)"
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
