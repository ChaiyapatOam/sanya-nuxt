<template>
  <!-- Welcome -->
  <div class="text-center">
    <Header />
    <!-- Jumbotron -->
    <div class="p-5 text-center bg-light" style="margin-top: 58px">
      <h1 class="mb-3">Welcome</h1>
      <h2 class="mb-3">สวัสดีครับ...</h2>
      <!-- <a class="btn btn-primary" href="" role="button">Call to action</a> -->
    </div>
    <!-- Jumbotron -->
    <div class="mybox">
      <b-card-group deck>
        <b-card class="mybox">
          <b-card-text
            ><h4>
              I am a client <br />
              ฉันเป็นผู้ใช้บริการ
            </h4></b-card-text
          >
        </b-card>

        <b-card>
          <b-card-text
            ><h4>
              I am a legal freelancer <br />
              ฉันเป็นฟรีแลนซ์ด้านกฎหมาย
            </h4></b-card-text
          >
        </b-card>
      </b-card-group>

    </div>
    <div style="font-size: 30px">
      <b-icon-facebook></b-icon-facebook>
      <b-icon-instagram></b-icon-instagram>
      <b-icon-youtube></b-icon-youtube>
      <b-icon-twitter></b-icon-twitter>
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
export default {
  name: 'IndexPage',
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
