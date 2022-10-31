<template>
 <md-button
    v-on="$listeners"
    v-bind="$attrs"
    @click="onClick"
    :class="{
      'custom-class': useCustomClass,
      'md-icon-button':isIcon, 
      'md-raised': isRaised,
      'md-dense': isDense
    }"
    :disabled="disabled"
    :href="href"
    :md-ripple="ripple"
 >
  <slot></slot>
 </md-button>
</template>

<script>
/* eslint-disable */
export default {
  name: 'BaseButton',
  inheritAttrs: false,
  props: {
    useCustomClass: {
      type: Boolean,
      default: false,
    },

    /**
     * @description Triggered after a mouse click.
     */
    onClick: {
      type: Function,
      default: () => () => {},
    },
    
    /**
     * @description Enables the rounded-shape icon button.
     */
    isIcon: {
      type: Boolean,
      default: false
    },

    /**
     * @description Creates raised buttons with elevation.
     */
    isRaised: {
      type: Boolean,
      default: false
    },

    /**
     * @description A slight small variant of buttons. Useful to create a compact UI.
     */
    isDense: {
      type: Boolean,
      default: false
    },
    
    /** @description Disables the button and prevents its actions. */
    disabled: {
      type: Boolean,
      default: false,
    },

    /** @description Creates a anchor on the button. In this case the generated tag will be <a>. */
    href: {
      type: [String | Object],
      default: null
    },

    /** @description Enables/Disables the ripple effect. */
    ripple: {
      type: Boolean,
      default: true,
    },

    /** @description Applies a type to button - It doesn't affects links. */
    type: {
      type: String,
      default: "button",
    },
  }
}
</script>

<style scoped>
.custom-class {
  background: rgb(107, 107, 107);
  background: linear-gradient(
    180deg,
    rgba(107, 107, 107, 1) 0%,
    rgba(30, 30, 30, 1) 100%
  );
}
</style>
