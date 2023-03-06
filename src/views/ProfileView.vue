<template>
  <div class="profile">
    <div class="profile__items">
      <div class="profile__items-section">
        <h1 class="hide-xs card-title">#10 Gabriel Meireles</h1>
        <player-card />
      </div>

      <div class="profile__items-section">
        <current-club />
      </div>

      <div class="profile__items-section">
        <national-team />
      </div>
    </div>

    <div class="profile__items--trophies">
      <player-trophies />
    </div>
  </div>
</template>

<script>
import PlayerCard from '../components/cards/PlayerCard.vue'
import CurrentClub from '../components/cards/CurrentClub.vue'
import PlayerTrophies from '../components/cards/PlayerTrophies.vue'
import NationalTeam from '../components/cards/NationalTeam.vue'

export default {
  name: 'profile-view',
  components: {
    PlayerCard,
    CurrentClub,
    PlayerTrophies,
    NationalTeam
  }
}
</script>

<style scoped lang="scss">
@import '@/assets/mixins';

.profile {
  display: flex;
  width: 100%;
  flex-direction: column;
  padding: 0 2rem;

  @include for-phone-only {
    flex-direction: column;
    align-items: flex-start;
  }

  &__items {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;

    @include for-phone-only {
      flex-direction: column;
    }

    &-section {
      h1 {
        margin-bottom: 10px;
      }

      @include for-tablet-portrait-up {
        &:nth-child(2) {
          padding: 50px;
        }
      }

      @include for-phone-only {
        width: 100%;
        margin-bottom: 40px;
      }
    }

    &__row {
      display: flex;
      width: 100%;
    }

    &--trophies {
      margin-top: 30px;
    }
  }
}
</style>
