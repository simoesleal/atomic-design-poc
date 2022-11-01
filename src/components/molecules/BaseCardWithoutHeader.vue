<template>
  <BaseCard>
    <template #card-content>
      <BaseContent>
        <slot name="content"></slot>
      </BaseContent>
    </template>
    <template #card-actions>
      <BaseContent>
        <slot name="actions"></slot>
      </BaseContent>
    </template>
  </BaseCard>
</template>
<script>
export default {
  name: 'BaseCardWithoutHeader',
}
</script>
<style scoped>
</style>