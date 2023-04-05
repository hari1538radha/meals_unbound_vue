<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    {{ msg }}
  </div>
</template>

<style scoped>

</style>
