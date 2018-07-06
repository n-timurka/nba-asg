<template>
  <section>
    <router-link to="player">
      <span class="player-name">{{ player.name }}</span>
      <img :src="playerImg"/>
      <img width="60" class="team-logo" :src="teamImg"/>
      <span class="player-number">#{{ player.jersey }}</span>
    </router-link>
  </section>
</template>

<script>
export default {
  name: 'PlayerCard',
  props: ['player'],
  computed: {
    playerImg () {
      return 'https://ak-static.cms.nba.com/wp-content/uploads/headshots/nba/latest/260x190/' + this.player.id + '.png'
    },
    teamImg () {
      return 'https://i.cdn.turner.com/nba/nba/assets/logos/teams/primary/web/' + this.player.team + '.svg'
    }
  }
}
</script>

<style scoped>
section {
  background: #fff;
  display: flex;
  position: relative;
  margin: 5% 0;
}
section * {
  text-decoration: none;
  color: #34495e;
}
section .player-name {
  font-size: 26px;
}
section .player-number {
  position: absolute;
  left: 0;
  bottom: 0;
  font-size: 34px;
  padding: 5px;
}
section .team-logo {
  position: absolute;
  right: 0;
  bottom: 0;
}
</style>
