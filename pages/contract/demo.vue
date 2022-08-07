<template>
  <div>
    <div class="row min-h">
      <div
        class="col-xl bg-white container mx-auto center text-primary text-center"
      >
        <div class="">
          <h2>สัญญาเช่าห้อง</h2>
          <!-- <h4>ลงชื่อเข้าสู่ระบบ</h4> -->
          <form @submit.prevent="handleSubmit" class="auth-form">
            <div class="form-group">
              <label for="address">สัญญาฉบับนี้ทำขึ้น ณ</label>
              <input
                type="text"
                id="address"
                class="form-control"
                required
                v-model="room_rent.create_At"
              />
            </div>

            <div class="form-group">
              <label for="create_Time">เมื่อวันที่</label>
              <b-input-group class="mb-3">
                <b-form-input
                  id="create_Time"
                  v-model="room_rent.create_Time"
                  type="text"
                  placeholder="วันที่"
                  autocomplete="off"
                ></b-form-input>
                <b-input-group-append>
                  <b-form-datepicker
                    v-model="room_rent.create_Time"
                    button-only
                    right
                    locale="th-TH"
                    aria-controls="create_Time"
                    @context="onContext"
                  ></b-form-datepicker>
                </b-input-group-append>
              </b-input-group>
            </div>

            <!-- Owner -->
            <h4>ผู้ให้เช่า</h4>
            <div class="form-group">
              <label for="name">ชื่อผู้ให้เช่า</label>
              <input
                type="text"
                id="name"
                class="form-control"
                required
                v-model="room_rent.owner.name"
              />
            </div>

            <div class="form-group">
              <label for="address">เลขประจำตัวประชาชนผู้ให้เช่า</label>
              <input
                type="text"
                id="address"
                class="form-control"
                required
                v-model="room_rent.owner.id"
              />
            </div>

            <div class="form-group">
              <label for="address">อายุผู้ให้เช่า</label>
              <input
                type="number"
                id="address"
                class="form-control"
                required
                v-model="room_rent.owner.age"
              />
            </div>

            <div class="form-group">
              <label for="address">ที่อยู่ให้เช่า</label>
              <input
                type="text"
                id="address"
                class="form-control"
                required
                v-model="room_rent.owner.address"
              />
            </div>

            <!-- Renter -->
            <h4>ผู้เช่า</h4>
            <div class="form-group">
              <label for="address">เลขประจำตัวประชาชนผู้เช่า</label>
              <input
                type="text"
                id="address"
                class="form-control"
                required
                v-model="room_rent.renter.id"
              />
            </div>

            <div class="form-group">
              <label for="address">อายุผู้เช่า</label>
              <input
                type="text"
                id="address"
                class="form-control"
                required
                v-model="room_rent.renter.age"
              />
            </div>

            <div class="form-group">
              <label for="address">ที่อยู่เช่า</label>
              <input
                type="text"
                id="address"
                class="form-control"
                required
                v-model="room_rent.renter.address"
              />
            </div>

            <!-- <button type="submit" class="btn btn-primary rounded-pill">
              เสร็จสิ้น
            </button> -->
          </form>
        </div>
      </div>

      <div class="col-xl bg-white container mx-auto center text-primary">
        <b-card-group deck>
          <b-card class="mt-3" header="Form Data Result">
            <pre class="m-0">{{ room_rent }} {{ formatted }}</pre>
          </b-card>
          <br />
          <b-card class="mt-3" header="สัญญาเช่าห้อง">
            <b-card-body>
              สัญญาฉบับนี้ทำขึ้น ณ
              <b
                ><u>{{ room_rent.create_At }}</u></b
              >
              เมื่อ
              <b>
                <u>{{ formatted }}</u>
              </b>
              <br />
              <b>
                <u>{{ room_rent.owner.name }}</u>
              </b>
              ซึ่งเป็นผู้ถือบัตรประชาชนเลขที่ {{ room_rent.owner.id }}
            </b-card-body>
          </b-card>
        </b-card-group>
      </div>
    </div>
  </div>
</template>

<script>
import Docs from '../../components/Docs.vue'
export default {
  data: () => ({
    formatted: '',
    selected: '',
    room_rent: {
      create_At: '',
      create_Time: null,
      owner: {
        name: '',
        id: '',
        age: 0,
        address: '',
      },
      renter: {
        name: '',
        id: '',
        age: 0,
        address: '',
      },
    },
  }),
  methods: {
    handleSubmit: () => {},
    onContext(ctx) {
      // The date formatted in the locale, or the `label-no-date-selected` string
      this.formatted = ctx.selectedFormatted
      // The following will be an empty string until a valid date is entered
      this.selected = ctx.selectedYMD
    },
  },
  components: { Docs },
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
p {
  width: 20px;
  border-bottom: 1px solid black;
}
</style>
