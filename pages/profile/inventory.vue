<template>
  <div>
    <div class="p-5 bg-primary text-white">
      <h1>กระเป๋าของคุณ</h1>
      <div class="progress" style="height: 0.25rem">
        <div
          class="progress-bar bg-danger"
          role="progressbar"
          style="width: 15%"
          aria-valuenow="20"
          aria-valuemin="0"
          aria-valuemax="100"
        ></div>
      </div>
      <ul>
        <li>
          <span class="badge bg-white text-primary rounded-circle">1</span>
          <u>กระเป๋าของคุณ</u>
        </li>
        <li>
          <span class="badge bg-white text-primary rounded-circle">2</span>
          การชำระเงิน
        </li>
      </ul>
    </div>
    <div class="row min-h">
      <div class="col-xl bg-white container mx-auto center text-primary">
        <div class="flex-2">
          <p>กระเป๋าของคุณ</p>
          <p>รวม (2 รายการ)</p>
        </div>
        <table class="table table-sm table-hover">
          <thead>
            <tr></tr>
          </thead>
          <tbody>
            <tr>
              <td>
                <div class="row">contract</div>
                <div class="row">
                  <img
                    src="https://picsum.photos/536/354"
                    width="50"
                    height="55"
                    alt=""
                  />
                  Contract
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="col-xl bg-white container mx-auto center text-primary">
        <div class="">
          <p class="">สรุปคำสั่งซื้อ</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
ul {
  padding: 0px;
}
li {
  display: inline-block;
  width: auto;
  list-style: outside none none;
}
.min-h {
  min-height: calc(100vh - 6.5rem);
}

.flex-center {
  display: flex;
  flex-direction: column;
  justify-items: center;
  align-items: center;
  gap: 1rem;
}
.flex-2 {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.auth-form {
  display: flex;
  flex-direction: column;
  justify-items: center;
  align-items: center;
  gap: 1rem;
}
</style>
