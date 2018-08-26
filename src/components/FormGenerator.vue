<template>
  <div id="form-generator">
    <ObjectNode :model="data"/>
  </div>
</template>

<script>
  import ObjectNode from './Node/ObjectNode';

  export default {
    name: "FormGenerator",
    components: {ObjectNode},
    props: {
      data: {
        type: Object,
        default: () => {},
      },

      components: {
        ObjectNode,
      }
    },
  }
</script>

<style lang="scss" scoped>
  #form-generator {
    border: 1px solid black;
  }
</style>