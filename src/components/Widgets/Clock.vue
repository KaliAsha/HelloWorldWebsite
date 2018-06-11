<template>
    <span class="widget-clock">{{ clock.substring(0, long ? 8 : 5) }}</span>
</template>

<script>
export default {
  props: {
    long: Boolean
  },
  data () {
    return {
      time: new Date(),
      longMode: this.long
    }
  },
  computed: {
    clock () {
      return this.time.toTimeString()
    }
  },
  mounted () {
    this.startClock()
  },
  methods: {
    startClock () {
      setInterval(() => {
        this.time = new Date()
      }, 1000)
    }
  }
}
</script>
