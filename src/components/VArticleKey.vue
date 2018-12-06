<template>
  <div>
    <div class="row flex-spaces border border-primary shadow shadow-hover margin margin-top-none margin-bottom-none">
      <div class="sm-1 col">
        <i class="fa fa-arrows-alt" />
      </div>
      <div class="sm-11 col">
        <div class="row margin-none">
          <div class="sm-4 col padding-bottom-none padding-top-none">
            <div class="form-group">
              <label>
                Name
              </label>
              <input
                class="input-block"
                type="text"
              >
            </div>
          </div>
          <div class="sm-4 col padding-bottom-none padding-top-none">
            <div class="form-group">
              <label>
                Type
              </label>
              <input
                class="input-block"
                type="text"
              >
            </div>
          </div>
          <div class="sm-4 col padding-bottom-none padding-top-none padding-right-none">
            <fieldset class="form-group">
              <legend>Options</legend>
              <label class="paper-check">
                <input
                  type="checkbox"
                  value="required"
                > <span>Required</span>
              </label>
              <label class="paper-check">
                <input
                  type="checkbox"
                  value="conditional"
                > <span>Conditional</span>
              </label>
            </fieldset>
          </div>
        </div>
        <div class="row padding-none margin-none">
          <div class="xs-12 col padding-none">
            <VDescription />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VDescription from '@/components/VDescription'

export default {
  name: 'VArticleKey',
  components: {
    VDescription,
  },
}
</script>

<style lang="scss">
.form-group {
  margin-bottom: 0 !important;
}
</style>
