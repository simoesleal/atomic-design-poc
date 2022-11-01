<template>
 <md-dialog-alert
  v-bind="$attrs"
  :md-active="activator"
  :md-content="content"
  :md-confirm-text="confirmText" />
</template>

<script>
  export default {
    name: 'BaseDialog',
    inheritAttrs: false,

    props: {
        activator: {
          default: undefined
        },

        content: {
          type: String,
        },

        confirmText: {
          type: String
        }
    }
  }
</script>