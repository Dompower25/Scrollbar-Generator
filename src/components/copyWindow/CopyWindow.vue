<script setup lang="ts">
defineProps({
  execution: {
    type: Boolean,
    default: true,
  },
});
</script>

<template>
  <div class="copyWind">
    <div class="shell">
      <img
        v-if="execution"
        class="img"
        src="../../assets/copyWindow/copySuccessfully.svg"
        alt="copy"
      />

      <img
        v-else
        class="img"
        src="../../assets/copyWindow/copyUnsuccessfully.svg"
        alt="copy"
      />

      <div v-if="execution" class="textInformation">copy is successfully</div>
      <div v-else class="textInformation">copy error</div>
    </div>
  </div>
</template>

<style lang="scss">
.copyWind {
  position: absolute;

  bottom: 30px;
  right: 30px;
  background: rgba(0, 0, 0, 0.03);

  box-sizing: border-box;

  border: 1px solid rgba(0, 0, 0, 0.07);
  background: rgba(0, 0, 0, 0.15);
  border-radius: 4px;

  font-family: "Inter", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;

  .shell {
    margin: 6px 8px;

    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-self: center;

    .img {
      width: 22px;
      height: 22px;

      padding-right: 10px;
    }

    .textInformation {
      color: rgba(255, 255, 255, 0.78);
      text-transform: uppercase;
      align-self: center;
    }
  }
}
</style>
