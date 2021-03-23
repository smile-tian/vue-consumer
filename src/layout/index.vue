<template>
  <el-container>
    <el-header>
      <Header/>
    </el-header>
    <el-main>
      <transition name="fade-transform" mode="out-in">
        <router-view :key="key"/>
      </transition>
    </el-main>
    <el-footer>
      <Footer/>
    </el-footer>
  </el-container>
</template>

<script>
import {Footer, Header} from './components'

export default {
  name: "Layout",
  components: {
    Footer,
    Header
  },
  computed: {
    key() {
      return this.$route.path
    }
  }
}
</script>

<style scoped>

</style>
