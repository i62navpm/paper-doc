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
          <div class="option-block xs-4 sm-5 col margin-small">
            <p style="font-size: 3rem;">
              <span style="color: rgba(2, 2, 2, 0.6)">
                <i class="fas fa-file-upload" />
              </span>
            </p>
            <span>
              Upload your Html
            </span>
          </div>
          <div
            class="option-block xs-4 sm-5 col margin-small"
            @click.prevent="goToDoc"
          >
            <p style="font-size: 3rem;">
              <span style="color: rgba(2, 2, 2, 0.6)">
                <i class="fas fa-pen-alt" />
              </span>
            </p>
            <span>
              Write your doc
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheInitModal',
  data: () => {
    return {
      open: false,
    }
  },
  methods: {
    goToDoc() {
      this.open = false
      setTimeout(() => this.$router.push({name: 'about'}), 200)
    }
  }
}
</script>

<style lang="scss" scoped>
@media only screen and (min-width: 768px) {
  .modal .modal-body {
      width: 30rem;
  }
}

.option-block {
  cursor: pointer;
  text-align: center;
}
</style>

