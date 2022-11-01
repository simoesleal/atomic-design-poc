<template>
  <md-card>
    <slot name="card-header"></slot>
    <slot name="card-content"></slot>
    <slot name="card-actions"></slot>
  </md-card>
</template>

<script>
export default {
  name: "BaseCard",
  inheritAttrs: false,
};
</script>
