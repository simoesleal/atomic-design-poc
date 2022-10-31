<template>
  <div id="app">
     <BaseButton
      @click="clicked"
      :isRaised="true"
      :isIcon="false"
      :ripple="true"
      :useCustomClass="true"
     >Btn</BaseButton>
     <BaseInput
      v-model="someInput"
    >1</BaseInput>
  </div>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    someInput: ''
  }),

  methods: {
    clicked(e) {
      console.log(e)
    }
  }
}
</script>

<style>
</style>
