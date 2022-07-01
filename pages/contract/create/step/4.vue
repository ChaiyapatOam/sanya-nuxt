<template>
  <div>
    <Header />
    <div class="jumbotron">
      <div class="row">
        <div class="col-sm-8 offset-sm-2">
          <div>
            <h2 class="text-center">สร้างร้านค้าของคุณ</h2>
            <form @submit.prevent="handleSubmit">
              <p>
                ถ้าบนที่ดินมีสิ่งปลูกสร้างอยู่แล้วสัญญานี้ครอบคลุมถึงสิ่งปลูกสร้างดังกล่าวด้วยหรือไม่
                <br />
                มีสิ่งปลูกสร้างบนพื้นที่หรือไม่
              </p>
              <div class="form-group">
                <div class="row">
                  <b-form-checkbox>มีสิ่งปลูกสร้าง</b-form-checkbox>
                  <b-form-checkbox class="mb-2 mr-sm-2 mb-sm-0"
                    >ไม่มีสิ่งปลูกสร้าง</b-form-checkbox
                  >
                </div>
                <input
                  type="text"
                  v-model="user.store"
                  id="store"
                  name="store"
                  placeholder="ชื่อผู้จะซื้อ"
                  class="form-control"
                  :class="{ 'is-invalid': submitted && $v.user.store.$error }"
                />
              </div>

              <!-- เลขประจำตัวประชาชนผู้ซื้อ -->
              <div class="form-group">
                <!-- <label for="address">เลขประจำตัวประชาชนผู้ซื้อ</label> -->
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="เลขประจำตัวประชาชนผู้ซื้อ"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />
              </div>
              <!-- อายุ -->
              <div class="form-group">
                <!-- <label for="address">เลขประจำตัวประชาชนผู้ซื้อ</label> -->
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="อายุผู้จะซื้อ"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />
              </div>

              <!-- ที่อยู่ผู้จะซื้อ -->
              <div class="form-group">
                <!-- <label for="address">เลขประจำตัวประชาชนผู้ซื้อ</label> -->
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="ที่อยู่ผู้จะซื้อ"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />
              </div>

              <!-- button  -->
              <div class="form-group text-center">
                <button class="btn btn-primary text-center">หน้า 4/7</button>
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
      date: '',
    }
  },
}
</script>
