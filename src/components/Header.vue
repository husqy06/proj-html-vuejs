<template>
  <header>
    <img src="../assets/img/construction_logo.png" class="logo">

    <ul>
      <li v-for="(item, index) in navItem" :key="index">
        <a :href="item.href" :class="item.href == 'current' ? 'current-link' : ''">{{ item.text }}</a>
      </li>
      <li><span class="small-botton">get quote</span></li>
    </ul>
  </header>
</template>

<script>
import { navItem } from '../assets/data.js'

export default {
  name: 'Header',
  data() {
    return {
      navItem,
    }
  }
}
</script>

<style scoped lang="scss">
@import '../style/general.scss';
</style>
