<template>
  <div class="matchup-tile">
    <Fixture :home="home" :away="away"></Fixture>
    <p>Reason: {{reason}}</p>
  </div>
</template>

<script>

import Fixture from 'components/fixture';

export default {
  name: 'MatchupTile',
  props: ['id', 'home', 'away', 'reason'],
  components: { Fixture }
}
</script>

<style>
.matchup-tile {
  padding: 40px 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.2);
}
</style>
