<template>
  <div>
    <div class="row min-h">
      <div class="col-xl bg-info container mx-auto center text-white">
        <h1>เข้าสู่ระบบ</h1>
      </div>

      <div class="col-xl bg-white container mx-auto center text-primary">
        <div class="flex-center">
          <h4>ลงชื่อเข้าสู่ระบบ</h4>
          <form @submit.prevent="handleSubmit" class="auth-form">
            <div class="form-group">
              <label for="username">ชื่อบัญชี</label>
              <input
                type="text"
                id="username"
                class="form-control"
                required
                v-model="username"
              />
            </div>

            <div class="form-group">
              <label for="password">รหัสผ่าน</label>
              <input
                type="password"
                id="password"
                class="form-control"
                required
                v-model="password"
              />
            </div>

            <!-- <div class="form-check font-weight-light">
              <input type="checkbox" id="remember-me" />
              <label for="remember-me" class="form-check-label"
                >จดจำการเข้าสู่ระบบ</label
              >
            </div> -->

            <!-- 2 column grid layout -->
            <div class="row mb-4">
              <div class="col-md-6 d-flex justify-content-center">
                <!-- Checkbox -->
                <div class="form-check mb-3 mb-md-0">
                  <input
                    class="form-check-input bg-primary"
                    type="checkbox"
                    value=""
                    id="loginCheck"
                    checked
                  />
                  <label class="form-check-label" for="loginCheck">
                    จดจำการเข้าสู่ระบบ
                  </label>
                </div>
              </div>

              <div class="col-md-6 d-flex justify-content-center">
                <!-- Simple link -->
                <a href="#" class="text-danger">ลืมรหัสผ่าน?</a>
              </div>
            </div>
                <p>
                  หากคุณยังไม่เป็นสมาชิก
                  <nuxt-link to="/register">สมัครสมาชิก</nuxt-link>
                </p>
              <button type="submit" class="btn btn-primary rounded-pill ">
                เข้าสู่ระบบ
              </button>

            <!-- <div class="flex">
              <button type="submit" class="btn btn-primary ">
                เข้าสู่ระบบ
              </button>
              <button class="btn btn-secondary">ลืมรหัสผ่าน</button>
            </div> -->
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
    username: '',
    password: '',
  }),
  methods: {
    handleSubmit: () => {},
  },
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
  justify-items: center;
  align-items: center;
  gap: 1rem;
}
nuxt-link {
  color: blue;
}
</style>
