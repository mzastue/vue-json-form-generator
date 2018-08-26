<template>
  <input
          class="boolean-node"
          type="checkbox"
          :value="value"
          :checked="value"
  >
</template>

<script>
  export default {
    name: "BooleanNode",

    props: {
      value: Boolean,
    }
  }
</script>

<style scoped>

</style>