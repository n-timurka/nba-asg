<template>
  <div id="app">
    <app-header/>
    <div class="teams-header">
      <div class="container">
        <h2>Team LeBron</h2>
        <h2>Team Stephen</h2>
      </div>
    </div>
    <transition name="fade">
      <router-view/>
    </transition>
  </div>
</template>

<script>
import AppHeader from '@/components/Header'
export default {
  name: 'App',
  components: {
    AppHeader
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Open+Sans');

body {
  font-family: 'Open Sans', sans-serif;
  margin: 0;
}
.container {
  max-width: 1024px;
  margin: 0 auto;
  position: relative;
}
#app {
  text-align: center;
  color: #2c3e50;
  background: #f2f3f5;
  overflow: hidden;
}
.teams-header {
  background: #fff;
  box-shadow: 0 1px 2px rgba(0,0,0,.1);
}
.teams-header .container {
  display: flex;
}
.teams-header h2 {
  width: 50%;
}
</style>
