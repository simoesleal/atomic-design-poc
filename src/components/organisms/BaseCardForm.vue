<template>
  <BaseCardWithHeader>
    <template #header>
      <BaseSubTitle :value="'Base Card Form Title'"></BaseSubTitle>
    </template>
    <template #content>
      <div class="md-layout">
        <slot name="form-content"></slot>
      </div>
    </template>
    <template #actions>
      <slot name="action"></slot>
    </template>
  </BaseCardWithHeader>
</template>
<script>
export default {
  name: 'BaseCardForm'
}
</script>
<style scoped>
</style>