<template>
  <BaseCard>
    <template #card-header>
      <BaseCardHeader>
        <slot name="header"></slot>
      </BaseCardHeader>
    </template>
    <template #card-content>
      <BaseCardContent>
        <slot name="content"></slot>
      </BaseCardContent>
    </template>
    <template #card-actions>
      <BaseCardActions>
        <slot name="actions"></slot>
      </BaseCardActions>
    </template>
  </BaseCard>
</template>
<script>
export default {
  name: 'BaseCardWithHeader',
}
</script>
<style scoped>
</style>