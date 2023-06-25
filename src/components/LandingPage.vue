<template>
  <div>

<!-- I used the name 'default' for the coloring, therefore the variant I renamed to 'simple' -->

<!-- for the icons, the prop should send the name of the material icon and it will be displayed automatically -->

<!-- I combined the colors with each variant and hover effect -->

  <ButtonComponent  :variant="'simple'" :color="'default'" :endIcon="'face'"  >
  My button
  </ButtonComponent </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
export default {
  name: 'LandingPage',
  components:{
    ButtonComponent
  },
}
</script>

<style scoped>

</style>
