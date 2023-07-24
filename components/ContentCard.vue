<template>
    <div class="ContentCard">
        <div class="card__logo"></div>
        <div class="card__content"></div>
        <div class="card__image"></div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.ContentCard {
    background-color: rgba(32, 33, 35);
    place-content: center flex-start;
    align-items: center;
    /* background-color: rgb(33, 35, 37); */
    border-radius: 24px;
    display: flex;
    flex: 0 0 auto;
    flex-flow: column nowrap;
    gap: 24px;
    /* height: 630px; */
    overflow: hidden;
    padding: 32px;
    position: relative;
    /* width: 592px; */
    /* will-change: transform; */
}
</style>