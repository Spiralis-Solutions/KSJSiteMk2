<template>
  <div id="q-app">
    <navbar></navbar>
    <router-view />
  </div>
</template>

<script>
import Navbar from './components/Navbar'
import AOS from 'aos'
export default {
  name: 'App',
  components: {
    'navbar': Navbar
  },
  created () {
    AOS.init()
  }
}
</script>

<style>
</style>
