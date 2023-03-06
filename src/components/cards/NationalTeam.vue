<template>
  <div class="national-team">
    <div>
      <img :src="flag" :alt="name" />
    </div>

    <div>
      <p><strong>Apps: </strong>{{ apps }}</p>
      <p><strong>Goals: </strong>{{ goals }}</p>
      <p><strong>Assists: </strong>{{ assists }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'national-team',
  data() {
    return {
      flag: 'https://tmssl.akamaized.net/images/wappen/homepageWappen150x150/3439.png?lm=1621002439',
      name: 'Brazil',
      apps: 60,
      goals: 10,
      assists: 5
    }
  }
}
</script>

<style scoped lang="scss">
.national-team {
  display: flex;
  flex-direction: row;
  align-items: center;
}
</style>
