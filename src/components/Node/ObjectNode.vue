<template>
  <div class="object-container">
    <div v-for="(value, objectProperty, index) in model" :key="`${objectProperty}-${index}`">
      {{ objectProperty }}
      <ObjectNode
          v-if="isObject(value)"
          :model="value"
      />

      <TextNode
              v-if="isText(value)"
              :value="value"
      />

      <NumberNode
              v-if="isNumber(value)"
              :value="value"
      />

      <BooleanNode
              v-if="isBoolean(value)"
              :value="value"
      />
    </div>
  </div>
</template>

<script>
  import TextNode from './TextNode';
  import NumberNode from './NumberNode';
  import BooleanNode from './BooleanNode';

  export default {
    name: "ObjectNode",

    props: {
      model: {
        type: Object|Array,
        default: () => {},
      },

      label: {
        type: String,
        default: '',
      }
    },

    components: {
      TextNode,
      NumberNode,
      BooleanNode,
    },

    methods: {
      isObject (value) {
        return typeof value === 'object';
      },

      isText (value) {
        return typeof value === 'string';
      },

      isNumber (value) {
        return typeof value === 'number';
      },

      isBoolean (value) {
        return typeof value === 'boolean';
      }
    }
  }
</script>

<style scoped>
  .object-container {
    border-bottom: 1px solid black;
  }
</style>