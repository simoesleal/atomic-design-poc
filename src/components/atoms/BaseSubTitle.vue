<template>
 <h3>{{value}}</h3>
</template>
<script>
export default {
  name: 'BaseSubTitle',
  inheritAttrs: false,
  props: {
    /** @description Value of the title */
    value: {
      type: String,
      default: null,
      required: true
    },
  },
}
</script>
<style scoped>
</style>