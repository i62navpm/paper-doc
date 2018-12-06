<template>
  <div>
    <TheInitModal ref="modal" />
  </div>
</template>

<script>
import TheInitModal from '@/components/TheInitModal'

export default {
  name: 'Home',
  components: {
    TheInitModal,
  },
  mounted() {
    this.$refs.modal.open = true
  },
}
</script>
