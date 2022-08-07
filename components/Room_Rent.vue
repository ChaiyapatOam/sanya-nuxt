<template>
  <div class="template">
    <div class="header">
      <div contenteditable>
        <h1>INTERACT {{content}}</h1>
      </div>
    </div>
    <!-- <vue-document-editor :content.sync="mycontent" /> -->
  </div>
</template>

<script>
import VueDocumentEditor from 'vue-document-editor'

export default {
  components: { VueDocumentEditor },
  props: ['content'],
  data() {
    return {
      mycontent: [`${this.content}`],
    }
  },
}
</script>
