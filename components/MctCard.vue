<template>
  <div class="card" :style="{ 'max-width': cardMW }">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'MctCard',
  props: {
    cardMW: {
      type: String,
      required: true
    },
  },
}
</script>

<style scoped>
.card {
  background-color: #161618;
  box-shadow: 0 4px 8px 0 #161618;
  transition: 0.3s;
  border-radius: 15px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #252529;
}
</style>