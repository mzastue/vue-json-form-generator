<template>
  <input
          type="text"
          :value="value"
  >
</template>

<script>
  export default {
    name: "TextNode",

    props: {
      value: {
        type: String,
        default: '',
      },
    }
  }
</script>

<style scoped>

</style>