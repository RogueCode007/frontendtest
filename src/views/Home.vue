<template>
  <div class="home">
    <MobileNav class="lg:hidden"/>
    <NavBar  class="hidden lg:block"/>
    <PinkBox />
    <FeatureBox />
    <Subscribe />
    <WhiteBox />
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import MobileNav from '@/components/MobileNav.vue'
import NavBar from '@/components/NavBar.vue'
import PinkBox from '@/components/PinkBox.vue'
import FeatureBox from '@/components/FeatureBox.vue'
import Subscribe from '@/components/Subscribe.vue'
import Footer from '@/components/Footer.vue'
import WhiteBox from '@/components/WhiteBox/WhiteBox'
export default {
  name: 'Home',
  components: {
    MobileNav, NavBar, PinkBox, FeatureBox, Subscribe, WhiteBox, Footer
  }
}
</script>
