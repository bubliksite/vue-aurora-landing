<template>
  <div class="main">
    <Menu />
    <MainScreen />
    <ToWhomInteresed />
    <WhatToTalk />
    <Speaker />
    <FormatWebinara class="format-webinara" />
    <OldWebinars />
    <Form />
    <Footer />
  </div>
</template>

<script>
  import Menu from '../components/Menu'
  import MainScreen from '../components/MainScreen'
  import ToWhomInteresed from '../components/ToWhomInteresed'
  import WhatToTalk from '../components/WhatToTalk'
  import Speaker from '../components/Speaker'
  import FormatWebinara from '../components/FormatWebinara'
  import Form from '../components/Form'
  import Footer from '../components/Footer'
  import OldWebinars from '../components/OldWebinars'
  export default {
    name: 'Home',
    components: {
      OldWebinars,
      Footer,
      Form,
      FormatWebinara,
      Speaker,
      WhatToTalk,
      ToWhomInteresed,
      MainScreen,
      Menu
    }
  }
</script>
