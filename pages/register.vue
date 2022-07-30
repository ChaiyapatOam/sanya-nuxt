<template>
  <div>
    <div class="row min-h">
      <div class="col-xl bg-info container mx-auto center text-white">
        <h1>สมัครสมาชิก</h1>
      </div>

      <div class="col-xl bg-white container mx-auto center text-primary">
        <div class="flex-center">
          <h4>สมัครสมาชิก</h4>
          <form @submit.prevent="handleSubmit" class="auth-form">

            <div class="form-group">
              <label for="email">อีเมล</label>
              <input type="email" id="email" class="form-control" required v-model="email">
            </div>

            <div class="form-group">
              <label for="password">รหัสผ่าน</label>
              <input type="password" id="password" class="form-control" required v-model="password">
            </div>

            <div class="form-group">
              <label for="password">ยืนยันรหัสผ่าน</label>
              <input type="password" id="password" class="form-control" required v-model="confirmPassword">
            </div>

            <div class="form-check font-weight-light">
              <input type="checkbox" id="remember-me">
              <label for="remember-me" class="form-check-label">ฉันได้อ่านและยอมรับ ข้อตกลงและเงื่อนไขการให้บริการของเรา</label>
            </div>

            <div class="form-check  font-weight-light">
              <input type="checkbox" id="remember-me">
              <label for="remember-me" class="form-check-label">ฉันได้อ่านและยอมรับ นโยบายคุ้มครองความเป็นส่วนตัว</label>
            </div>

            <div class="form-check  font-weight-light">
              <input type="checkbox" id="remember-me">
              <label for="remember-me" class="form-check-label">ฉันสนใจรับข้อมูลข่าวสาร ส่วนลด และ โปรโมชั่นจาก สํญญา</label>
            </div>

            <div class="flex">
              <button type="submit" class="btn btn-primary">สมัครสมาชิก</button>
            </div>
          </form>
        </div>
      </div>
    </div>

    <!-- <div class="mt-5 pt-5 mb-5 text-center">
    <button type="button" class="btn btn-primary">Primary</button>
    <button type="button" class="btn btn-secondary">Secondary</button>
    <button type="button" class="btn btn-success">Success</button>
    <button type="button" class="btn btn-danger">Danger</button>
    <button type="button" class="btn btn-warning">Warning</button>
    <button type="button" class="btn btn-info">In fo</button>
    <button type="button" class="btn btn-light">Light</button>
    <button type="button" class="btn btn-dark">Dark</button>
    <button type="button" class="btn btn-link">Link</button>
  </div> -->
  </div>
</template>

<script>
export default {
  name: 'Login',
  data: () => ({
    email: '',
    password: '',
    confirmPassword: ''
  }),
  methods: {
    handleSubmit: () => {

    }
  }
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
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
</style>
