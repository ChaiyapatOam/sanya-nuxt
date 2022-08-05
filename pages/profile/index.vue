<template>
  <!-- Welcome -->
  <div class="text-center">
    <!-- Jumbotron -->
    <div class="p-5 bg-light row">
      <b-img
        src="https://picsum.photos/125/125/?image=58"
        rounded="circle"
      ></b-img>
      <h2 class="mb-3">ชื่อ-นามสกุล</h2>

      <!-- <a class="btn btn-primary" href="" role="button">Call to action</a> -->
    </div>
    <!-- Jumbotron -->

    <!-- Bio -->
    <div class="container text-center">
      <div class="">
        <h4>การศึกษา :</h4>
        <h4>อาศัยอยู่ที่ :</h4>
        <h4>จาก :</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Profile',
  components: {},
}
</script>
<style scoped>
/* Write Css */
b-card-group b-card:hover {
  background-color: aquamarine;
}
b-card-group.mybox:hover {
  background-color: aquamarine;
}
</style>
