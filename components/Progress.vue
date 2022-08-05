<template>
  <div class="p-5 bg-primary text-white">
    <h1>กระเป๋าของคุณ</h1>
    <div class="progress" style="height: 0.25rem">
      <div
        class="progress-bar bg-danger"
        role="progressbar"
        style="width: 15%"
        aria-valuenow="20"
        aria-valuemin="0"
        aria-valuemax="70"
      ></div>
    </div>
    <ul class="">
      <li v-for="(p, i) in progress" :key="i">
        <span class="dot text-primary">{{ p.no }}</span>
        {{ p.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Progress',
  data() {
    return {
      progress: [
        { no: 1, name: 'วันที่และสถานที่ทำสัญญา' },
        {
          no: 2,
          name: 'ข้อมูลผู้จะขาย',
        },
        {
          no: 3,
          name: 'ข้อมูลผู้จะซื้อ',
        },
        {
          no: 4,
          name: 'ข้อมูลที่ดิน',
        },

        {
          no: 5,
          name: 'ราคาที่ดิน',
        },
        {
          no: 6,
          name: 'ค่าธรรมเนียม',
        },
        {
          no: 7,
          name: 'อื่นๆ',
        },
      ],
    }
  },
}
</script>

<style scoped>
ul {
  padding: 1px;
  display: flex;
  flex-direction: row;
}
li {
  display: inline-block;
  width: auto;
  list-style: outside none none;
  margin-right: 3%;
}

.dot {
  height: 25px;
  width: 25px;
  background-color: white;
  border-radius: 50%;
  display: inline-block;
  text-align: center;
}
</style>
