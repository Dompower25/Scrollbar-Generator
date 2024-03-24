<script setup lang="ts"></script>

<template>
  <div class="wrapper">
    <div class="scrollbar_style_block">
      <section>
        <div class="scrollbar_box">
          <div class="scrollbar">
            <img src="../assets/Group 11.svg" alt="scrollbar" />
          </div>
          <div class="inputs_scrollbar_styles">
            <div class="input_scrollbar_style">24px</div>
            <div class="input_scrollbar_style">color picker</div>
            <div class="input_scrollbar_style">8px</div>
            <div class="input_scrollbar_style">color picker</div>
            <div class="input_scrollbar_style">2px</div>
            <div class="input_scrollbar_style">color picker</div>
            <div class="input_scrollbar_style">border style picker</div>
          </div>
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

      align-items: center;
    }

    .scrollbar_box {
      position: absolute;
      display: flex;
      justify-content: space-around;
      align-items: center;

      padding: 15px 0px;

      .scrollbar {
        position: relative;
        width: 30px;
        height: 322px;
        background: rgba(255, 255, 255, 0.1);
        
        img {
          position: relative;
          transform: translate(-23px, 20px);
        }
        
      }

      .inputs_scrollbar_styles {
        position: relative;
        transform: translate(20px, -32px);

        display: flex;
        flex-direction: column;




        .input_scrollbar_style {
          position: relative;
          top: 5px;
          padding: 9px 4px;
        
          font-family: "Inter", sans-serif;
          font-optical-sizing: auto;
          font-weight: 300;

          color: rgba(255, 255, 255, 0.78);
          font-weight: 400;
          font-size: 14px;

          border-bottom: 1px solid rgba(255, 255, 255, 0.2);
          width: 200px; // возможно потребуется удалить, при использовании интутов.
        }

      }

    }

    // border: 1px solid white;
  }

  .css_style_block {
    width: 100%;
    height: 100%;

    border: 1px solid yellow;
  }
}
</style>
