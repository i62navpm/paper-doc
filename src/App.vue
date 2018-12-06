<template>
  <div id="app">
    <TheNavBar />
    <div class="container">
      <RouterView />
    </div>
  </div>
</template>

<script>
import TheNavBar from '@/components/TheNavBar'

export default {
  components: {
    TheNavBar,
  },
}
</script>


<style lang="scss" scoped>
.container {
  margin-top: 4rem;
}
</style>
