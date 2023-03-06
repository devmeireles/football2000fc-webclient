<template>
  <div class="wrapper">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'wrapper'
}
</script>

<style scoped lang="scss">
@import '@/assets/mixins';
.wrapper {
  background-color: #fff;
  min-height: 100vh;
  margin: 2rem 3rem;
  padding: 3rem 0;

  @include for-phone-only {
    margin: 1rem;
  }
}
</style>
