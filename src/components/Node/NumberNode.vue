<template>
  <input
          type="number"
          :value="value"
  >
</template>

<script>
  export default {
    name: "NumberNode",

    props: {
      value: Number,
    }
  }
</script>

<style scoped>

</style>