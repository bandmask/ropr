<template>
  <div class="home">
    <h1>ropr.se</h1>
    <div class="intro">
      <h3>Hi and welcome!</h3>
      <div>Glad to see you have found the home and playground belonging to <a href="mailto:niklasjsson@gmail.com" title="niklasjsson@gmail.com">me</a>.</div>
      <div>As of now the site is under construction and may feel kind of empty. This will hopefully change, soon.</div>
      <div>In the meantime, checkout an ongoing project for updates concerning this year's rum calendar <a href="https://daysofrum.ropr.se" target="_blank" title="24DaysOfRum">@24DaysOfRum</a></div>
      <Gallery :images="vm.images" class="gallery" />
    </div>
  </div>
</template>

<script>
import Gallery from '@/components/gallery/Gallery'
import imgHomeDaysOfRumLogo from '@/assets/daysofrumlogo.png'

export default {
  name: 'home',
  components: { Gallery },
  data () {
    return {
      images: [{
        src: imgHomeDaysOfRumLogo,
        name: '24DaysOfRum',
        description: '2018 24DaysOfRum Box'
      }]
    }
  },
  computed: {
    vm () {
      return this
    }
  }
}
</script>

<style scoped lang="less">
.intro {
  margin-top: 50px;
  h3 {
    margin: 40px 0 0;
  }
  a {
    color: #0aa;
    font-style: italic;
  }

  .gallery {
    margin-top: 40px;
  }
}
</style>
