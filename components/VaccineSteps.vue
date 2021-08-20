<template>
  <div class="text-center">
    <h2 class="text-4xl font-bold mb-6">Register for Vaccine</h2>
    <p class="text-lg">You will just need your NID Card, Phone number and filling up some info </p>
    <div class="flex -mx-6 my-16">
      <div class="flex-1 px-6">
        <div class="h-32 flex justify-center items-center">
          <img class="mx-auto" src="~/static/img/promo-1.svg" alt="">
        </div>
        <div class="border-4 w-6 h-6 rounded-full border-green-600 mx-auto mb-4 mt-8 tika-step relative"></div>
        <p class="font-bold text-lg">NID</p>
      </div>

      <div class="flex-1 px-6">
        <div class="h-32 flex justify-center items-center">
          <img v-if="theme == 'homepage' || theme == 'step_2' || theme == 'step_3'" class="mx-auto" src="~/static/img/promo-2.svg" alt="">
          <img v-if="theme == 'step_1'" class="mx-auto" src="~/static/img/promo-2-disabled.svg" alt="">
        </div>
        <div v-bind:class="theme == 'homepage' || theme == 'step_2 ' || theme == 'step_3' ? 'border-green-600' : 'border-gray-400'" class="border-4 w-6 h-6 rounded-full mx-auto mb-4 mt-8 tika-step relative"></div>
        <p class="font-bold text-lg">Phone</p>
      </div>

      <div class="flex-1 px-6">
        <div class="h-32 flex justify-center items-center">
          <img v-if="theme == 'homepage' || theme == 'step_3' " class="mx-auto" src="~/static/img/promo-3.svg" alt="">
          <img v-if="theme == 'step_1' || theme == 'step_2'" class="mx-auto" src="~/static/img/promo-3-disabled.svg" alt="">
        </div>
        <div v-bind:class="theme == 'homepage' || theme == 'step_3' ? 'border-green-600' : 'border-gray-400'" class="border-4 w-6 h-6 rounded-full  mx-auto mb-4 mt-8 tika-step relative"></div>
        <p class="font-bold text-lg">Information</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "VaccineSteps",
  props: ["theme"]
}
</script>

<style scoped>

</style>
