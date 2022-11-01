<template>
  <md-field>
    <label>
      <slot></slot>
    </label>
    <md-input
      v-on="listeners"
      v-bind="$attrs"
      @input="updateValue"
      :value="value"
    >
    </md-input>
  </md-field>
</template>
<script>
export default {
  name: 'BaseInput',
  inheritAttrs: false,
  props: {
    /** @description The input's value. */
    value: {}
  },

  computed: {
    /**
     * @description This method is necessary to work with multiple actions, like blur, touch, and input events.
     * The last executed is the one with more priority.
     */
    listeners() {
      return {
        ...this.$listeners,
        input: this.updateValue,
      };
    },
  },

  methods: {
    /**
     * @description Take the event that is happening
     *              and emit the event to the parent.
     */
    updateValue(event) {
      this.$emit("input", event);
    },
  },
}
</script>
<style scoped>
</style>