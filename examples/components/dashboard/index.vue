<template>
  <mw-frame :showMobileSide.sync="showMobileSide">
    <mw-brand slot="brand">
      Strawes
    </mw-brand>
    <mw-navigation slot="navigation">
      <mw-menu :list="menu"></mw-menu>
    </mw-navigation>
    <div slot="information">
      <mw-profile label="周聪" :avator="avator">
      </mw-profile>
    </div>
    <router-view slot="contents"></router-view>
    <mn-assistive-bar slot="footer" :show.sync="showMobileSide"></mn-assistive-bar>
  </mw-frame>
</template>

<script>
  import assistiveBar from 'vue-human/suites/assistiveBar'

  export default {
    data () {
      return {
        menu: require('./menu').default,
        avator: 'https://ois1yok9v.qnssl.com/example-avator.png',
        showMobileSide: false
      }
    },
    components: {
      ...assistiveBar.map()
    }
  }
</script>
