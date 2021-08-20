<template>
  <div>
    <div class="primary-bg text-white pb-10 text-lg text-center">
      <div class="container mx-auto">
        <h2 class="text-4xl font-bold mb-6">Vaccine Registration</h2>
        <p>Complete the registration by verifying your national identity card and mobile number in the form below. The place and date of delivery of the vaccine will be informed in due course through SMS message on the mobile phone.</p>
      </div>
    </div>

    <div class="py-20">
        <div class="small-container mx-auto">
          <VaccineSteps :theme="step"/>

          <div class="bg-white px-20 py-10 border border-gray-100">
            <div v-if="step == 'step_1'" class="">
              <h3 class="font-bold text-4xl mb-6 text-center">Identity Verification</h3>

              <div v-if="peopleData.hasOwnProperty('success') && !peopleData.success" class="bg-red-200 text-red-900 p-4 mb-6">
                {{ peopleData.message }}
              </div>


              <p class="mb-6">
                <label class="tika-label" for="category_id">Select category </label>
                <select v-model="verifyData.category_id" class="tika-input" id="category_id">
                  <option selected="selected" value="">Select a category</option>
                  <option v-for="item in categories" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>

              <div v-if="verifyData.category_id" class="flex -mx-4">
                <div class="w-2/3 px-4">
                  <p class="mb-6">
                    <label for="id_no" class="tika-label">National ID Number</label>
                    <input id="id_no" v-model="verifyData.id_no" type="number" class="tika-input" placeholder="Type your national ID card number">
                  </p>
                </div>
                <div class="w-1/3 px-4">
                  <p class="mb-6">
                    <label for="dob" class="tika-label">Date of birth</label>
                    <input id="dob" v-model="verifyData.dob" type="date" class="tika-input" placeholder="Type your national ID card number">
                  </p>
                </div>
              </div>

              <p><button @click.prevent="checkMyInformation" class="primary-btn">Check my information</button></p>
            </div>

            <div v-if="step == 'step_2'" class="">
              <h3 class="font-bold text-4xl mb-6 text-center">User Information</h3>

              <p class="mb-6">
                <label class="tika-label" for="category_id">Select division </label>
                <select @change.prevent="getAvailableDistricts" v-model="division_id" class="tika-input" id="division_id">
                  <option selected="selected" value="">Select a division</option>
                  <option v-for="item in divisions" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>

              <p v-if="districts.length" class="mb-6">
                <label class="tika-label" for="category_id">Select district </label>
                <select v-model="district_id" class="tika-input" id="district_id">
                  <option selected="selected" value="">Select a district</option>
                  <option v-for="item in districts" :key="item.id" :value="item.id">{{item.name}}</option>
                </select>
              </p>
            </div>

          </div>
        </div>
    </div>

    <div class="container mx-auto">
      <ThreeSteps/>
    </div>
  </div>
</template>

<script>
import VaccineSteps from "../components/VaccineSteps";
import ThreeSteps from "../components/ThreeSteps";
export default {
  name: "registration",
  components: {ThreeSteps, VaccineSteps},
  data() {
    return {
      categories: [],
      divisions: [],
      districts: [],
      step: 'step_2',
      peopleData: [],
      verifyData: {
        category_id: '',
        id_no: '',
        dob: ''
      },
      district_id: '',
      division_id: ''
    }
  },
  mounted() {
    this.getAvailableCategory();
    this.getAvailableDivisions();
  },
  methods: {
    getAvailableCategory() {
      this.$axios.get('/categories').then(res => {
        this.categories = res.data
      })
    },

    getAvailableDivisions() {
      this.$axios.get('/divisions').then(res => {
        console.log(res.data)
        this.divisions = res.data
      })
    },
    checkMyInformation() {
      this.$axios.post('/verify', this.verifyData).then(res => {
        console.log(res.data)
        this.peopleData = res.data;
        if(res.data.success) {
          this.step = 'step_2'
        }
      })
    },
    getAvailableDistricts() {
      this.$axios.get('/districts?division_id=' + this.division_id).then(res => {
        this.districts = res.data
      })
    },
  }
}
</script>

<style scoped>

</style>
