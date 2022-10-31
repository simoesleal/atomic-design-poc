<template>
  <div id="app">
     <BaseButton
      @click="clicked"
      :isRaised="true"
      :isIcon="false"
      :ripple="true"
      :useCustomClass="true"
     >Btn</BaseButton>
  </div>
</template>

<script>

export default {
  name: 'App',

  data: () => ({}),

  methods: {
    clicked(e) {
      console.log(e)
    }
  }
}
</script>

<style>
</style>
