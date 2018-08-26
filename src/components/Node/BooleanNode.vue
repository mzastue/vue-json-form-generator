<template>
  <input
          class="boolean-node"
          type="checkbox"
          :value="value"
          :checked="value"
  ></input>
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