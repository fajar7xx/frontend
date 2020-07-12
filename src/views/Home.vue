<template>
  <div class="home">
    <Header/>
    <Sliders/>
    <ItemSliders/>
    <InstaSection/>
    <LogoSection/>
    <Footer/>
  </div>
</template>

<script>
  // @ is an alias to /src
  import Header from '@/components/Header'
  import Sliders from '@/components/Sliders'
  import ItemSliders from '@/components/ItemSliders'
  import InstaSection from '@/components/InstaSection'
  import LogoSection from '@/components/LogoSection'
  import Footer from '@/components/Footer'

  export default {
    name: 'Home',
    components: {
      Header,
      Sliders,
      ItemSliders,
      InstaSection,
      LogoSection,
      Footer
    }
  }
</script>
