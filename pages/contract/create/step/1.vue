<template>
  <div>
    <Header />
    <div class="jumbotron">
      <div class="row">
        <div class="col-sm-8 offset-sm-2">
          <div>
            <h2 class="text-center">สร้างร้านค้าของคุณ</h2>
            <form @submit.prevent="handleSubmit">
              <div class="form-group">
                <label for="store">เลือกโปรไฟล์ที่ต้องการทำสัญญา</label>
                <input
                  type="text"
                  v-model="user.store"
                  id="store"
                  name="store"
                  class="form-control"
                  :class="{ 'is-invalid': submitted && $v.user.store.$error }"
                />
                <div
                  v-if="submitted && !$v.user.store.required"
                  class="invalid-feedback"
                >
                  โปรดใส่ชื่อร้าน
                </div>
              </div>

              <!-- ที่อยู่ร้าน -->
              <div class="form-group">
                <label for="address">สัญญาฉบับนี้ทำขึ้น ณ</label>
                <textarea
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />
                <div
                  v-if="submitted && !$v.user.address.required"
                  class="invalid-feedback"
                >
                  โปรดใส่ที่อยู่ร้าน
                </div>
              </div>

              <!-- Date -->
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

              <!-- button  -->
              <div class="form-group text-center">
                <button class="btn btn-primary text-center">หน้า 1/7</button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'

export default {
  name: 'Profile',
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      user: {
        store: '',
        email: '',
        phone: '',
        password: '',
        confirmPassword: '',
        address: '',
      },
      submitted: false,
      date:''
    }
  },
}
</script>
