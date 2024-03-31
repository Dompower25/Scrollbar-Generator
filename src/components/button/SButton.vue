<script setup lang="ts">

defineProps({
    innerText: {
        type: String,
        default: "inner-Text",
        required: true
    },
    colorText: {
        type: String,
        default: "black",
        required: true
    },
    backgroundColor: {
        type: String,
        default: "none",
        required: true
    },

})


</script>



<template>
    <button class="wrapperButton" :style="{ color: colorText, background: backgroundColor }">
        {{ innerText }}
    </button>
</template>


<style lang="scss">
.wrapperButton {

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

    &:first-child{
        margin-left: 0px !important;
    }

    &:last-child {
        margin-right: 0px !important;
    }

    &:active {
        text-shadow: 2px 1px 2px rgba(89, 137, 185, 0.836) !important;
    }
    
    cursor: pointer;    
    
}

</style>