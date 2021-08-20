<template>
  <div class="relative">
    <div class="primary-bg pt-2 pb-24">
      <div class="container mx-auto">
        <div class="flex items-center">
          <div class="w-full">
            <h1 class="hero-heading font-bold text-white uppercase leading-none mb-6">Vaccine</h1>
            <h2 class="text-7xl font-medium text-white mb-10">Registration</h2>
            <p class="text-white text-2xl">Complete the registration by verifying your national identity card and mobile number</p>
          </div>
          <div class="min-w-max">
            <img width="600" src="~/static/img/bro.png" alt="">
          </div>
        </div>
      </div>
    </div>
    <div class="relative">
      <div class="dots-1 absolute left-10 top-10"></div>
      <div class="container mx-auto small-container text-center py-20">
        <div class="">
          <VaccineSteps theme="homepage"/>

          <div class="text-left mb-16">
            <h2 class="text-4xl font-bold mb-6">Get Updates</h2>
            <p class="text-lg">Check Your Registration Status, Vaccine card, Certificate and See Faqs .</p>
          </div>

          <div class="flex -mx-4">
            <div class="flex-1 px-4">
              <nuxt-link to="" class="block shadow-xl border border-gray-200 px-6 pt-16 pb-10 relative">
                <div class="flex justify-center items-center h-32">
                  <img src="~/static/img/box-1.svg" class="" alt="">
                </div>
                <p class="text-lg font-semibold mt-6">Check Status</p>

                <div class="absolute left-0 -bottom-5 w-full"><img class="mx-auto" src="~/static/img/enter-1.svg" alt=""></div>
              </nuxt-link>
            </div>

            <div class="flex-1 px-4">
              <nuxt-link to="" class="block shadow-xl border border-gray-200 px-6 pt-16 pb-10 relative">
                <div class="flex justify-center items-center h-32">
                  <img src="~/static/img/box-2.svg" class="" alt="">
                </div>
                <p class="text-lg font-semibold mt-6">Vaccine card</p>

                <div class="absolute left-0 -bottom-5 w-full"><img class="mx-auto" src="~/static/img/enter-2.svg" alt=""></div>
              </nuxt-link>
            </div>

            <div class="flex-1 px-4">
              <nuxt-link to="" class="block shadow-xl border border-gray-200 px-6 pt-16 pb-10 relative">
                <div class="flex justify-center items-center h-32">
                  <img src="~/static/img/box-3.svg" class="" alt="">
                </div>
                <p class="text-lg font-semibold mt-6">Certificate</p>

                <div class="absolute left-0 -bottom-5 w-full"><img class="mx-auto" src="~/static/img/enter-3.svg" alt=""></div>
              </nuxt-link>
            </div>

            <div class="flex-1 px-4">
              <nuxt-link to="" class="block shadow-xl border border-gray-200 px-6 pt-16 pb-10 relative">
                <div class="flex justify-center items-center h-32">
                  <img src="~/static/img/box-4.svg" class="" alt="">
                </div>
                <p class="text-lg font-semibold mt-6">FAQs</p>

                <div class="absolute left-0 -bottom-5 w-full"><img class="mx-auto" src="~/static/img/enter-4.svg" alt=""></div>
              </nuxt-link>
            </div>



          </div>
        </div>


      </div>
    </div>

    <div class="container mx-auto">
      <div class="primary-bg text-white mx-auto rounded-3xl py-20 px-16">
        <div class="flex items-center">
          <div class="w-1/3 mr-10 font-bold">
            <h3 class="text-7xl uppercase">Hotline</h3>
            <p class="text-4xl">Numbers</p>
          </div>
          <div class="w-2/3">
            <div class="flex flex-wrap -mx-8">
              <div class="w-1/2 px-8 mb-8">
                <div class="bg-white p-4 rounded-lg text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-2">
                      <img src="~/static/img/phone-pink.svg" alt="">
                    </div>
                    <div class="w-full">
                      <h4 class="tika-text-pink text-4xl font-bold">333</h4>
                      <p class="text-xl">National Call Center</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="w-1/2 px-8 mb-8">
                <div class="bg-white p-4 rounded-lg text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-2">
                      <img src="~/static/img/phone-green.svg" alt="">
                    </div>
                    <div class="w-full">
                      <h4 class="tika-text-primary text-4xl font-bold">16263</h4>
                      <p class="text-xl">Health Portal</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="w-1/2 px-8">
                <div class="bg-white p-4 rounded-lg text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-2">
                      <img src="~/static/img/phone-orange.svg" alt="">
                    </div>
                    <div class="w-full">
                      <h4 class="tika-text-orange text-4xl font-bold">10655</h4>
                      <p class="text-xl">IEDCR</p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="w-1/2 px-8">
                <div class="bg-white p-4 rounded-lg text-black">
                  <div class="flex items-center">
                    <div class="min-w-max mr-2">
                      <img src="~/static/img/phone-blue.svg" alt="">
                    </div>
                    <div class="w-full">
                      <h4 class="tika-text-blue text-4xl font-bold">09666777222</h4>
                      <p class="text-xl">Covid-19 Telehealth</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <ThreeSteps/>
    </div>


    <div class="primary-bg text-center text-white text-2xl font-bold py-20">
      <div class="container mx-auto">
        <div class="flex">
          <div class="flex-1 px-10">
            <h3 class="font-bold text-5xl mb-4">10,000,000</h3>
            <p>Registered</p>
          </div>

          <div class="flex-1 px-10">
            <h3 class="font-bold text-5xl mb-4">8,000,000</h3>
            <p>Vaccinated</p>
          </div>

          <div class="flex-1 px-10">
            <h3 class="font-bold text-5xl mb-4">7,000,000</h3>
            <p>Certificate Issued</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VaccineSteps from "../components/VaccineSteps";
import ThreeSteps from "../components/ThreeSteps";
export default {
  components: {ThreeSteps, VaccineSteps},
  data() {
    return {

    }
  },
  mounted() {

  },
  methods: {

  }
}
</script>
