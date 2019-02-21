<template>
  <div>
    <h1>About Page!</h1>
    <h2>ipSite: {{ ip }}</h2>
  </div>
</template>
<script>
export default {
  async asyncData({ $axios, req, res }) {
    const ip = await $axios.$get('http://icanhazip.com')
    console.log(ip)
    return { ip }
  }
  // data: function() {
  //   return {
  //     ip: ''
  //   }
  // },
  // async created() {
  //   const ip = await this.$axios.$get('http://icanhazip.com')
  //   this.ip = ip
  // }
}
</script>
