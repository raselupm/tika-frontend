<template>
  <div>
    <h1 v-if="apiValue" class="font-bold text-3xl">Check: {{apiValue}}</h1>
    <button @click.prevent="testBackendRequest">Request API</button>
    <Tutorial/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      apiValue: ''
    }
  },
  mounted() {

  },
  methods: {
    testBackendRequest() {
      this.$axios.get('/test').then(res => {
        this.apiValue = res.data;
      });
    }
  }
}
</script>
