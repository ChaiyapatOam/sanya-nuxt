<template>
  <!-- Welcome -->
  <div class="text-center">
    <!-- Jumbotron -->
    <div class="p-5 text-center text-info">
      <h1 class="mb-3">Welcome</h1>
      <h2 class="mb-3">สวัสดีครับ...</h2>
    </div>

    <!-- Jumbotron -->
    <div class="mybox container mx-auto py-5">
      <b-card-group deck>
        <nuxt-link to="/login" class="card">
          <div class="card-body">
            <h4 class="font-weight-light">
              I am a client <br />
              ฉันเป็นผู้ใช้บริการ
            </h4>
          </div>
        </nuxt-link>

        <nuxt-link to="/login" class="card">
          <div class="card-body">
            <h4 class="font-weight-light">
              I am a legal freelancer <br />
              ฉันเป็นฟรีแลนซ์ด้านกฎหมาย
            </h4>
          </div>
        </nuxt-link>
      </b-card-group>
    </div>
    <div style="font-size: 30px; color: #1d434c" class="my-5">
      <b-icon-facebook></b-icon-facebook>
      <b-icon-instagram></b-icon-instagram>
      <b-icon-youtube></b-icon-youtube>
      <b-icon-twitter></b-icon-twitter>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  components: {},
}
</script>
<style scoped>
a.card {
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}

div.card-body a {
  text-decoration: none;
  color: #1d434c;
}
.card-deck a {
  color: #1d434c;
  text-decoration: none;
}
.card-deck a:hover {
  background-color: #1d434c;
  color: white;
  text-decoration: none;
}

/* div.card :hover {
  color: white;

} */
</style>
