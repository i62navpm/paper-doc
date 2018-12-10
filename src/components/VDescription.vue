<template>
  <div class="row margin-none">
    <div class="col sm-12 padding-bottom-none padding-top-none">
      <div class="collapsible margin-top-small">
        <input
          id="collapsible"
          type="checkbox"
          name="collapsible"
        >
        <label for="collapsible">
          Description
        </label>
        <div class="collapsible-body">
          <Editor
            v-model="description"
            preview-style="vertical"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { Editor } from '@toast-ui/vue-editor'

export default {
  name: 'VDescription',
  components: {
    Editor,
  },
  data: function() {
    return {
      description: '# hello',
    }
  },
}
</script>
