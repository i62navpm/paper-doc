<template>
  <div class="row margin-none">
    <div class="col sm-6 padding-bottom-none padding-top-none">
      <div class="form-group">
        <label>Description</label>
        <textarea
          class="input-block"
          :value="input"
          @input="update"
        />
      </div>
    </div>

    <div class="col sm-6 padding-bottom-none padding-top-none">
      <div class="collapsible margin-top-large">
        <input
          id="collapsible"
          type="checkbox"
          name="collapsible"
        >
        <label for="collapsible">
          View Markdown
        </label>
        <div class="collapsible-body">
          <div v-html="compiledMarkdown" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import marked from 'marked'
import debounce from 'lodash.debounce'

export default {
  name: 'VDescription',
  data: function() {
    return {
      input: '# hello',
    }
  },
  computed: {
    compiledMarkdown: function() {
      return marked(this.input, { sanitize: true })
    },
  },
  methods: {
    update: debounce(function(e) {
      this.input = e.target.value
    }, 300),
  },
}
</script>
