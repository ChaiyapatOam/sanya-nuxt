<template>
  <!-- Welcome Homepage -->
  <div >
    <!-- Jumbotron -->
    <div class="bg-info">
      <div class="p-5 text-white container mx-auto">
        <h1 class="mb-3">ฟรี</h1>
        <h2 class="mb-3">บริการสร้าง "สัญญา" ด้วยตนเอง</h2>
        <h4 class="font-weight-light">> เลือก "สัญญา" ที่คุณต้องการ</h4>
        <h4 class="font-weight-light">> ตอบคำถาม (กรอกข้อมูลในสัญญา)</h4>
        <h4 class="font-weight-light">> ส่ง Invitation link สู่คู่สัญญา</h4>
        <h4 class="font-weight-light">> เซ็นทั้งสองฝ่าย</h4>
        <h5 class="text-danger">
          หมายเหตุ สามารถปรึกษาความถูกต้องของสัญญา กับสัญญาได้เพิ่มเติม*
        </h5>
        <a class="btn btn-primary bg-dark" href="" role="button">Click</a>
      </div>
    </div>
    <!-- Jumbotron -->

    <img src="~/assets/img/Sanya-Academy.png" style="text-align: center;" class="text-center" />
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      slide: 0,
      sliding: null,
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
  },
}
</script>
<style scoped>
/* Write Css */
</style>
