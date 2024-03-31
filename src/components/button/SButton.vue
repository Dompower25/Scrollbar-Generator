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
        default: "white",
        required: true
    },

})


</script>



<template>
    <div class="wrapperButton" :style="{ color: colorText, background: backgroundColor }">
        {{ innerText }}
    </div>
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

    border-radius: 3px;
    background: rgb(224, 219, 219);
    color: black;

    &:first-child{
        margin-left: 0px !important;
    }

    &:last-child {
        margin-right: 0px !important;
    }

}

</style>