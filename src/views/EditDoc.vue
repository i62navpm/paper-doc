<template>
  <div class="edit">
    <h1>Edit your doc</h1>
    <VSectionKey
      v-for="section in sections"
      :key="section.id"
      :section="section"
    />

    <div class="row flex-right">
      <div class="col xs-4 align-middle">
        <button
          class="btn-block"
          @click.prevent="addSection(++index)"
        >
          Add section <i class="fa fa-plus" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import VSectionKey from '@/components/VSectionKey'

export default {
  name: 'EditDoc',
  components: {
    VSectionKey,
  },
  data: () => ({
    index: 1,
    sections: [{ id: 1 }],
  }),
  methods: {
    addSection(id) {
      this.sections.push({ id })
    },
  },
}
</script>
