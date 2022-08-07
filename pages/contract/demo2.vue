<template>
  <div>
    <div class="row min-h">
      <div class="col-xl bg-white container mx-auto center text-primary">
        <form @submit.prevent="handleSubmit" class="auth-form">
          <div class="container vertical-scrollable">
            <div class="form-group">
              <label for="address">สัญญาฉบับนี้ทำขึ้น ณ</label>
              <input
                type="text"
                id="address"
                class="form-control"
                required
                v-model="user"
              />
            </div>

            <div class="form-group">
              <label for="phone">เมื่อวันที่</label>
              <b-input-group class="mb-3">
                <b-form-input
                  id="example-input"
                  v-model="date"
                  type="text"
                  placeholder="YYYY-MM-DD"
                  autocomplete="off"
                ></b-form-input>
                <b-input-group-append>
                  <b-form-datepicker
                    v-model="date"
                    button-only
                    right
                    locale="en-US"
                    aria-controls="example-input"
                    @context="onContext"
                  ></b-form-datepicker>
                </b-input-group-append>
              </b-input-group>
            </div>

            <button type="submit" class="btn btn-primary rounded-pill">
              เสร็จสิ้น
            </button>
          </div>
        </form>
      </div>

      <div class="col-xl bg-white container mx-auto center text-primary">
        {{ y }}
        <Docs :user="user" />
      </div>
    </div>
  </div>
</template>

<script>
import VueDocumentEditor from 'vue-document-editor'
import Docs from '~/components/Docs.vue'

export default {
  components: { VueDocumentEditor, Docs },
  data() {
    return {
      user: 'Kabigon',
      x: 1,
      y:  1,
    }
  },
  methods: {
    handleSubmit: () => {},
  },
}
</script>

<style scoped>
.min-h {
  min-height: calc(100vh - 6.5rem);
}

.center {
  display: grid;
  place-items: center;
}

.flex-center {
  display: flex;
  flex-direction: column;
  justify-items: center;
  align-items: center;
  gap: 1rem;
}

.auth-form {
  display: flex;
  flex-direction: column;
  justify-items: center;
  align-items: center;
  gap: 1rem;
}
.vertical-scrollable > .row {
  position: absolute;
  top: 120px;
  bottom: 100px;
  left: 180px;
  width: 50%;
  overflow-y: scroll;
}
</style>
