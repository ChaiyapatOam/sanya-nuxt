<template>
  <div>
    <Progress/>
    <div class="jumbotron">
      <div class="row">
        <div class="col-sm-8 offset-sm-2">
          <div>
            <h2 class="text-center"></h2>
            <form @submit.prevent="handleSubmit">
              <div class="form-group">
                <label for="store">ผู้จะซื้อ</label>
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
              <Step :page="3" />
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

import Step from '~/components/Step.vue'
import Progress from '~/components/Progress.vue'

export default {
  name: 'Profile',
  components: {
    Step,
    Progress
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
