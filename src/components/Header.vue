<template>
  <header>
    <div class="container">
      <p class="header">{{ header }}</p>
      <p class="info">{{ msg }}</p>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      header: 'Nba All-Stars 2017',
      msg: 'Made by Timurka Nick on VueJs Framework'
    }
  }
}
</script>

<style scoped>
header {
  background: #f60;
  color: #fff;
  text-align: left;
  height: 40px;
}
p.header {
  font-weight: normal;
  margin: 0;
  font-size: 20px;
  line-height: 40px;
}
p.info {
  position: absolute;
  font-size: 12px;
  right: 0;
  top: 0;
}
</style>
