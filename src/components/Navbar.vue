<template>
    <b-navbar toggleable="md" type="dark" variant="dark">

        <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

        <b-navbar-brand>KaliAsha</b-navbar-brand>

        <b-collapse is-nav id="nav_collapse">
            <b-navbar-nav>
                <b-nav-item href="#">Link</b-nav-item>
            </b-navbar-nav>

            <b-navbar-nav class="ml-auto">
                <b-nav-item @click.stop="changeDisplayClock"><Clock :long="clockLongDisplay"/></b-nav-item>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>
</template>

<script>
import Clock from './Widgets/Clock'

export default {
  components: {
    Clock
  },
  data () {
    return {
      clockLongDisplay: false
    }
  },
  methods: {
    changeDisplayClock () {
      this.clockLongDisplay = !this.clockLongDisplay
    }
  }
}
</script>
