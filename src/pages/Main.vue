<template>
  <main class="container">
    <div class="teams-players">
      <div class="team-block">
        <player-card :player="player"/>
        <player-card :player="player"/>
        <player-card :player="player"/>
        <player-card :player="player"/>
        <player-card :player="player"/>
      </div>
      <div class="team-block">
        <player-card :player="player"/>
        <player-card :player="player"/>
      </div>
    </div>
  </main>
</template>

<script>
import PlayerCard from '@/components/PlayerCard'
export default {
  name: 'Main',
  components: {
    PlayerCard
  },
  data () {
    return {
      player: {
        id: 203507,
        name: 'Giannis Antentokoumpo',
        team: 'MIL',
        jersey: 23,
        position: 'Forward'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.teams-players {
  display: flex;
}
.teams-players .team-block {
  width: 45%;
}
.teams-players .team-block:last-child {
  margin-left: 10%;
}
</style>
