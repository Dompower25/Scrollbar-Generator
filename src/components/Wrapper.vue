<script setup lang="ts"></script>

<template>
  <div class="wrapper">
    <div class="scrollbar_style_block">
      <section>
        <div class="scrollbar_box">
          <div class="scrollbar"></div>
        </div>
      </section>
    </div>
    <div class="line"></div>
    <div class="css_style_block"></div>
  </div>
</template>

<style lang="scss">
@import "../styles/index.scss";

.wrapper {
  width: 70%;
  height: 500px;

  border: 1px solid rgb(223, 120, 120);

  display: flex;
  justify-content: space-between;
  align-items: center;
  box-sizing: border-box;
  padding: 20px;



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



    section {
      height: 100%;
      display: flex;
      
      justify-content: space-around;
      align-items: center;
    }

    .scrollbar_box {
    width: 30px;
    height: 322px;
    background: rgba(255, 255, 255, 0.1);
    display: flex;
    justify-content: center;

    padding: 15px 0px;

    .scrollbar {
      width: 19px;
      height: 198px;
      border-radius: 10px;
      align-self: flex-end;
      background: rgba(29, 35, 56, 1);
    }
  }

    border: 1px solid white;
  }
  .css_style_block {
    width: 100%;
    height: 100%;

    border: 1px solid yellow;
  }
}
</style>
