<template>
  <div>
    <Progress/>
    <div class="jumbotron">
      <div class="row">
        <div class="col-sm-8 offset-sm-2">
          <div>
            <p></p>
            <form @submit.prevent="handleSubmit">
              <p>
                ใครเป็นผู้รับผิดชอบในค่าธรรมเนียมโอน อากรแสตมป์
                และค่าใช้จ่ายต่างๆ
              </p>

              <!-- ผู้รับผิดชอบค่าธรรมเนียมการโอน -->
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
                <label for="check"
                  >ในระหว่างการจ่ายเงินค่าซื้อที่ดิน
                  ผู้จะขายมีการทำสัญญาเช่ากับบุคคลใดๆหรือไม่</label
                >
                <b-form-checkbox-group
                  id="checkbox-group-1"
                  v-model="selected"
                  :options="check"
                  :aria-describedby="ariaDescribedby"
                  name="flavour-1"
                ></b-form-checkbox-group>
              </div>

              <Step :page="6" />
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
import Step from '~/components/Step.vue'
import Progress from '~/components/Progress.vue'

export default {
  name: 'Profile',
  components: {
    Header,
    Footer,
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
      selected: null,
      options: [
        { item: null, name: 'ผู้รับผิดชอบค่าธรรมเนียมการโอน' },
        { item: 'A', name: 'ฝ่ายละเท่าๆกัน' },
        { item: 'B', name: 'ผู้จะขายเป็นผู้รับผิดชอบ' },
        { item: 'D', name: 'ผู้จะซื้อเป็นผู้รับผิดชอบ' },
      ],
      check: [
        { text: 'มีการทำสัญญาเช่า', value: true },
        { text: 'ไม่มีการทำสัญญาเช่า', value: false },
      ],
    }
  },
}
</script>
