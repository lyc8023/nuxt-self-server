<template>
  <div>
    <h1>A Page</h1>
    <h1>project: {{ project }}</h1>
  </div>
</template>
<script>
export default {
  data() {
    console.dir('data')
    return { project: 'default' }
  },
  asyncData(context) {
    console.dir('asyncData')
    return { project: 'nuxt' }
  }
}
</script>
