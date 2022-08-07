<template>
  <div>
    <h1>{{user}}</h1>
    <input type="text" v-model="user">
    <vue-document-editor :content.sync="data" />
  </div>
</template>

<script>
import VueDocumentEditor from 'vue-document-editor'
import Room_Rent from './Room_Rent.vue'
import { markRaw } from 'vue'

export default {
  components: { VueDocumentEditor },
  props: ['user'],
  data() {
    return {
      data: [{ template: markRaw(Room_Rent), props: { content: this.user } }],
    }
  },
}
</script>
