<template>
    <div class="Card">
        <slot></slot>

    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.Card {
  background-color: rgba(32, 33, 35);
  place-content: center flex-start;
  align-items: center;
  justify-content: center;
  /* background-color: rgb(33, 35, 37); */
  border-radius: 24px;
  display: flex;
  /* flex: 0 0 auto; */
  flex-flow: column nowrap;
  gap: 32px;
  /* height: 630px; */
  overflow: hidden;
  padding: 32px;
  /* padding-bottom: 0; */
  position: relative;
  max-width: 592px;
  width: 100%;
  /* will-change: transform; */
  /* height: 200vh; */
}
</style>