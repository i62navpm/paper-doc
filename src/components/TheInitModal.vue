<template>
  <div>
    <input
      class="modal-state"
      type="checkbox"
      :checked="open"
    >
    <div class="modal">
      <label class="modal-bg" />
      <div class="modal-body">
        <label
          class="btn-close"
          @click.prevent="goToDoc"
        >
          X
        </label>
        <h4 class="modal-title">
          Doc Options
        </h4>
        <h5 class="modal-subtitle">
          What do you want to do?
        </h5>

        <div class="row flex-spaces child-borders child-shadows-hover">
          <VModalOption
            icon="fa-file-upload"
            message="Upload your Html"
            @click.native="goToDoc"
          />
          <VModalOption
            icon="fa-pen-alt"
            message="Write your doc"
            @click.native="goToDoc"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VModalOption from '@/components/VModalOption'

export default {
  name: 'TheInitModal',
  components: {
    VModalOption,
  },
  data: () => {
    return {
      open: false,
    }
  },
  methods: {
    goToDoc() {
      this.open = false
      setTimeout(() => this.$router.push({ name: 'edit' }), 200)
    },
  },
}
</script>

<style lang="scss" scoped>
@media only screen and (min-width: 768px) {
  .modal .modal-body {
    width: 30rem;
  }
}
</style>

