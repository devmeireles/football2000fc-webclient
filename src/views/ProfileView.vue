<template>
  <v-container fluid class="profile pa-0 pa-sm-12 bg-surface-variant">
    <v-row no-gutters class="align-end">
      <v-sheet class="ma-2 pa-2">
        <h1 class="hide-xs card-title mb-3">#10 Gabriel Meireles</h1>
        <player-card />
      </v-sheet>

      <v-sheet class="ma-2 pa-2">
        <current-club />
      </v-sheet>

      <v-sheet class="ma-2 pa-2">
        <national-team />
      </v-sheet>
    </v-row>

    <v-row no-gutters class="pt-10">
      <player-trophies />
    </v-row>

    <!-- <v-row no-gutters class="pt-10">
      <detailed-player-stats/>
    </v-row> -->
  </v-container>
</template>

<script>
import PlayerCard from '../components/cards/PlayerCard.vue'
import CurrentClub from '../components/cards/CurrentClub.vue'
import PlayerTrophies from '../components/cards/PlayerTrophies.vue'
import NationalTeam from '../components/cards/NationalTeam.vue'
import DetailedPlayerStats from '../components/tables/DetailedPlayerStats.vue'

export default {
  name: 'profile-view',
  components: {
    PlayerCard,
    CurrentClub,
    PlayerTrophies,
    NationalTeam,
    DetailedPlayerStats
  }
}
</script>

<style scoped lang="scss">
@import '@/assets/mixins';

.profile {
  @include for-phone-only {
    flex-direction: column;
    align-items: flex-start;
    padding: 0;
  }
}
</style>
