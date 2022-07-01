<template>
  <div>
    <Header />
    <div class="jumbotron">
      <div class="row">
        <div class="col-sm-8 offset-sm-2">
          <div>
            <p>สร้างร้านค้าของคุณ</p>
            <form @submit.prevent="handleSubmit">
              <p>ราคาที่ดิน</p>
              <div class="form-group">
                <input
                  type="text"
                  v-model="user.store"
                  id="store"
                  name="store"
                  placeholder="ราคาที่ดินทั้งสิ้น"
                  class="form-control"
                  :class="{ 'is-invalid': submitted && $v.user.store.$error }"
                />
              </div>
              <!-- แบ่งชำระเป็นกี่งวด -->
              <div class="form-group">
                <input
                  type="text"
                  v-model="user.store"
                  id="store"
                  name="store"
                  placeholder="แบ่งชำระเป็นกี่งวด"
                  class="form-control"
                  :class="{ 'is-invalid': submitted && $v.user.store.$error }"
                />
              </div>

              <!-- ชำระงวดแรก -->
              <div class="form-group">
                <label for="address">ชำระงวดแรก</label>
                <input
                  type="text"
                  v-model="user.address"
                  id="address"
                  name="address"
                  placeholder="จำนวนเงิน"
                  class="form-control"
                />
              </div>

              <!-- ชำระเป็น -->
              <div class="form-group">
                <b-form-select
                  v-model="selected"
                  :options="options"
                  class="mb-3"
                  value-field="item"
                  text-field="name"
                  disabled-field="notEnabled"
                ></b-form-select>
              </div>

              <!-- checkbox -->
              <div class="form-group">
                <label for="check">ในกรณีผิดนัดมีการคิดค่าปรับหรือไม่</label>
                <b-form-checkbox-group
                  id="checkbox-group-1"
                  v-model="selected"
                  :options="check"
                  :aria-describedby="ariaDescribedby"
                  name="flavour-1"
                ></b-form-checkbox-group>
              </div>

              <!-- button  -->
              <div class="form-group text-center">
                <button class="btn btn-primary text-center">หน้า 5/7</button>
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
      selected: null,
      options: [
        { item: null, name: 'ชำระเป็น' },
        { item: 'A', name: 'เงินสด' },
        { item: 'B', name: 'เช็คธนาคาร' },
        { item: 'D', name: 'โอนเข้าบัญชีธนาคาร' },
      ],
      check: [
        { text: 'คิดค่าปรับ', value: true },
        { text: 'ไม่คิดค่าปรับ', value: false },
      ],
    }
  },
}
</script>
