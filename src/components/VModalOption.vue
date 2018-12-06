<template>
  <div class="option-block xs-4 sm-5 col margin-small">
    <p style="font-size: 3rem;">
      <span style="color: rgba(2, 2, 2, 0.6)">
        <i
          class="fas"
          :class="icon"
        />
      </span>
    </p>
    <span>
      {{ message }}
    </span>
  </div>
</template>

<script>
export default {
  name: 'VModalOption',
  props: {
    message: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.option-block {
  cursor: pointer;
  text-align: center;
}
</style>
