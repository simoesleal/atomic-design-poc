<template>
  <div id="app">
    <BaseTitle :value="'Page Title'"></BaseTitle>
    <BaseCardForm>
      <template #form-content>
        <BaseInput
          v-model="someInput"
        >1</BaseInput>
      </template>
      <template #action>
      <BaseButton
        @click="cancel"
        :isRaised="true"
        :isIcon="false"
        :ripple="true"
        :useCustomClass="false"
      >Cancel</BaseButton>
      <BaseButton
        @click="clicked"
        :isRaised="true"
        :isIcon="false"
        :ripple="true"
        :useCustomClass="true"
      >Submit</BaseButton>
      </template>
    </BaseCardForm>
    {{ someInput }}
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
      alert(this.someInput)
    },

    cancel() {
      this.someInput = ''
    }
  }
}
</script>

<style>
</style>
