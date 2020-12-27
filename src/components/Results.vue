<template>
  <h1>{{ comment }}</h1>
  <p>Reaction time: {{ time }} ms</p>
</template>

<script>
  export default {
    data() {
      return {}
    },
    computed: {
      comment() {
        if (this.time < 250) return 'Ninja Fingers!'
        if (this.time < 400) return 'Rapid Reflexes'
        else if (this.time < 500) return 'Can be improved'
        else return 'Snail pace...'
      },
    },
    props: ['time'],
  }
</script>

<style></style>
