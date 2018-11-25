<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/architecture">Architecture</router-link>
    </div>
    <router-view class="component-content" />
    <Footer></Footer>
    <div v-if="vm.isDebug">{{this.$mq}}</div>
  </div>
</template>

<script>
import Footer from '@/modules/footer/Footer'

export default {
  components: { Footer },
  computed: {
    vm () {
      return this
    },
    isDebug () {
      return process.env.NODE_ENV !== 'production'
    }
  }
}
</script>

<style lang="less">
body {
  margin: 0;
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;

    #nav {
      position: absolute;
      top: 20px;
      left: 50px;

      padding: 10px;
      a {
        font-weight: bold;
        color: #2c3e50;
        &.router-link-exact-active {
          color: #0aa;
        }
      }
    }

    .component-content {
      padding: 20px 0px;
    }

    h1,
    h2,
    h3 {
      display: inline-block;
      margin: 10px 0px;
    }

    h3 {
      font-style: italic;
      margin-bottom: 0px;
    }

    p {
      margin: 5px 0px;
    }
  }
}
</style>
