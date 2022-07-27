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
                <label for="store">ผู้จะขาย</label>
                <input
                  type="text"
                  v-model="user.store"
                  id="store"
                  name="store"
                  placeholder="ชื่อผู้จะขาย"
                  class="form-control"
                  :class="{ 'is-invalid': submitted && $v.user.store.$error }"
                />

              </div>

              <!-- เลขประจำตัวประชาชนผู้ขาย -->
              <div class="form-group">
                <!-- <label for="address">เลขประจำตัวประชาชนผู้ขาย</label> -->
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="เลขประจำตัวประชาชนผู้ขาย"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />

              </div>
              <!-- อายุ -->
              <div class="form-group">
                <!-- <label for="address">เลขประจำตัวประชาชนผู้ขาย</label> -->
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="อายุผู้จะขาย"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />

              </div>

              <!-- ที่อยู่ผู้จะขาย -->
              <div class="form-group">
                <!-- <label for="address">เลขประจำตัวประชาชนผู้ขาย</label> -->
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="ที่อยู่ผู้จะขาย"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />

              </div>



              <!-- button  -->
              <div class="form-group text-center">
                <button class="btn btn-primary text-center">หน้า 2/7</button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>

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
