<template>
  <div class="current-club">
    <div class="current-club__body">
      <div class="current-club__body-club">
        <img :src="clubFlag" :alt="club" />
      </div>

      <div class="current-club__body-info">
        <p class="club">{{ club }} - {{ league }}</p>
        <p><strong>Joined: </strong>{{ joined }}</p>
        <p><strong>Contract: </strong>{{ contractDeadline }}</p>
        <p><strong>Market Value: </strong>{{ marketValue }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'current-club',
  data() {
    return {
      clubFlag: 'https://logodetimes.com/times/rayo-vallecano/logo-rayo-vallecano-1536.png',
      club: 'Rayo Vallecano',
      league: 'La Liga',
      country: 'Spain',
      joined: '10/10/2010',
      contractDeadline: 'Jun 2023',
      marketValue: '€50'
    }
  }
}
</script>

<style scoped lang="scss">
.current-club {
  &__body {
    display: flex;

    &-club {
      img {
        max-width: 120px;
      }
    }

    &-info {
      display: flex;
      flex-direction: column;
      padding-left: 15px;

      p.club {
        font-size: large;
        font-weight: 900;
      }
    }
  }
}
</style>
