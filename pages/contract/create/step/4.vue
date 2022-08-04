<template>
  <div>
    <Header />
    <div class="jumbotron">
      <div class="row">
        <div class="col-sm-8 offset-sm-2">
          <div>
            <h2 class="text-center"></h2>
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
                  placeholder="เลขที่โฉนด"
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
                  placeholder="ระวางที่ดิน"
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
                  placeholder="ตำบล"
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
                  placeholder="อำเภอ"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />
              </div>
              <!-- จังหวัด -->
              <div class="form-group">
                <!-- <label for="address">เลขประจำตัวประชาชนผู้ซื้อ</label> -->
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="จังหวัด"
                  class="form-control"
                  :class="{
                    'is-invalid': submitted && $v.user.address.$error,
                  }"
                />
              </div>
              <!-- ขนาดที่ดิน -->
              <div class="form-group">
                <label for="address">ขนาดที่ดิน</label>
                <div class="oneline">
                  <input
                    type="text"
                    v-model="user.address"
                    id="address"
                    name="address"
                    placeholder="ไร่"
                    class="form-control"
                    :class="{
                      'is-invalid': submitted && $v.user.address.$error,
                    }"
                    style="width: 10rem"
                  />
                  <input
                    type="text"
                    v-model="user.address"
                    id="address"
                    name="address"
                    placeholder="งาน"
                    class="form-control"
                    :class="{
                      'is-invalid': submitted && $v.user.address.$error,
                    }"
                    style="width: 10rem"
                  />
                  <input
                    type="text"
                    v-model="user.address"
                    id="address"
                    name="address"
                    placeholder="วา"
                    class="form-control"
                    :class="{
                      'is-invalid': submitted && $v.user.address.$error,
                    }"
                    style="width: 10rem"
                  />
                </div>
              </div>
              <Step :page="4" />
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
import Step from '~/components/Step.vue'

export default {
  name: 'Profile',
  components: {
    Header,
    Footer,
    Step,
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

<style scoped>
div.oneline {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
