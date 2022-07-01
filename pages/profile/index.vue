<template>
  <!-- Welcome -->
  <div class="text-center">
    <Header />
    <!-- Jumbotron -->
    <div class="p-5 bg-light row" style="margin-top: 58px">
      <b-img src="https://picsum.photos/125/125/?image=58" rounded="circle"></b-img>
      <h1 class="mb-3">Welcome</h1>
      <h2 class="mb-3">สวัสดีครับ...</h2>
      <b-btn class="primary" pill>แก้ไขโปรไฟล์</b-btn>
      <!-- <a class="btn btn-primary" href="" role="button">Call to action</a> -->
    </div>
    <!-- Jumbotron -->

    <!-- Bio -->
    <div class="container text-center">
        <div class="">
            <h4>การศึกษา : </h4>
            <h4>อาศัยอยู่ที่ : </h4>
            <h4>จาก : </h4>
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
