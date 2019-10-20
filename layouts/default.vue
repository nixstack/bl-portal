<template>
  <v-app>
    <Header />
    <!-- <v-container>
      <Nuxt />
    </v-container> -->
    <div :style="{ 'margin-top': isHome ? '192px' : '96px' }">
      <Nuxt />
    </div>
    <Footer />
  </v-app>
</template>

<script>
import Header from '../components/Header'
import Footer from '@/components/Footer'
export default {
  components: {
    Header,
    Footer
  },
  data() {
    return {
      isHome: false
    }
  },
  watch: {
    $route: {
      immediate: true,
      handler(to, from) {
        if (to && from && to.fullPath !== from.fullPath) {
          // window.location.reload()
          this.$router.go(to.fullPath)
        }
        // if (!this.$store.state.auth.account) {
        //   return this.$router.push('/')
        // }
      }
    }
  },
  mounted() {
    this.isHome = this.$route.path === '/'
  }
}
</script>
