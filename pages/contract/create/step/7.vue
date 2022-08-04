<template>
  <div>
    <div class="jumbotron">
      <div class="row">
        <div class="col-sm-8 offset-sm-2">
          <div>
            <p></p>
            <form @submit.prevent="handleSubmit">
              <p>ข้อสัญญาเพิ่มเติมอื่นๆ (ุถ้ามี)</p>

              <!-- ผู้รับผิดชอบค่าธรรมเนียมการโอน -->
              <div class="form-group">
                <b-form-checkbox
                  v-model="selected"
                  :aria-describedby="ariaDescribedby"
                  name="flavour-3a"
                >
                  ผู้จะขายรับรองว่าที่ดิน
                  เป็นกรรมสิทธิ์โดยชอบตามกฎหมายของผู้จะขาย
                </b-form-checkbox>
                <b-form-checkbox
                  v-model="selected"
                  :aria-describedby="ariaDescribedby"
                  name="flavour-3a"
                >
                  ไม่มีภาระผูกพันใดๆ บนที่ดิน
                  นอกเหนือจากที่เปิดเผยไว้ในสัญญาฉบับนี้
                </b-form-checkbox>
              </div>

              <!-- ปรึกษา -->
              <div class="form-group">
                <label for="check">ปรึกษาผู้เชี่ยวชาญกับทางทีมงานสัญญา</label>
                <p>- เพิ่มความมั่นใจ</p>
                <p>- ตรวจสอบความถูกต้องของสัญญา</p>
                <p>- พูดคุยและขอคำปรึกษาได้อย่างใกล้ชิด</p>
                <div class="check">
                  <b-form-checkbox id="checkbox-group-1" v-model="selected">
                    บริการเพิ่มเติมนัดปรึกษากับทางผู้เชี่ยวชาญ <br />
                    เป็นเวลา 30 นาที</b-form-checkbox
                  >
                  <p class="text-danger">300 บาท</p>
                </div>
              </div>

              <!-- button  -->
              <div class="form-group text-center">
                <b-btn pill style="background-color: #1d434c" class="text-white"
                  >เสร็จสิ้น</b-btn
                >
                <br />
                <p class="" style="margin-top: 25px">
                  <nuxt-link to="/contract/create/step/6">
                    <b-icon-arrow-left-circle-fill
                      style="cursor: pointer; font-size: 22px"
                    ></b-icon-arrow-left-circle-fill>
                  </nuxt-link>
                  &nbsp; หน้า 7/7 &nbsp;
                </p>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Profile',
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
<style scoped>
div.check {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
