<template>
  <div>
    <div class="row">
      <div class="col xs-12 padding-top-none padding-bottom-none">
        <div class="form-group margin-bottom-none">
          <label>Section title</label>
          <input
            class="input-block"
            type="text"
          >
        </div>
      </div>
    </div>
    <VArticleKey />
  </div>
</template>

<script>
import VArticleKey from '@/components/VArticleKey'

export default {
  name: 'VSectionKey',
  components: {
    VArticleKey,
  },
}
</script>

