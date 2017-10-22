<template>
  <div id="app">
    <h1>Marquee Matchup Predictions</h1>
    <p>FIFA 18 Ultimate Team (FUT) Unofficial Website, for people who want to MAKE COIN.</p>
    <MatchupTile
      v-for="(match, i) in matchups"
      key="i"
      :id="i"
      :home="match.home"
      :away="match.away"
      :reason="match.reason"></MatchupTile>
    <h4>How to make coin, you ask?</h4>
    <p>The matches featured here have a chance of being featured in the upcoming Marquee Matchups Squad Building Challenge. If you invest in the early, you can sell for big profit Monday/Tuesday night. Or, risk holding on to them for HUGE AMOUNTS OF COIN!</p>
  </div>
</template>

<script>
import matchups from 'data/matchups.yml';

import MatchupTile from 'components/matchup-tile';

export default {
  name: 'app',
  components: {
    MatchupTile
  },
  data: () => ({ matchups })
}
</script>

<style>
* {
  box-sizing: border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

a {
  color: #42b983;
}
</style>
