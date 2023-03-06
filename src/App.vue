<template>
  <headerbar />
  <wrapper>
    <router-view />
  </wrapper>
  <nav-footer />
</template>

<script>
import { RouterView } from 'vue-router'
import Wrapper from './components/containers/Wrapper.vue'
import Headerbar from './components/navigators/Headerbar.vue'
import NavFooter from './components/navigators/NavFooter.vue'

export default {
  name: 'app',
  components: {
    Wrapper,
    Headerbar,
    NavFooter
  }
}
</script>
