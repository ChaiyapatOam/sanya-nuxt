<template>
  <!-- /?lang=th -->
  <nav
    class="navbar navbar-expand-md navbar-light bg-light text-darkgreen fixed-top"
    id="NAV"
  >
    <div class="container-fluid">
      <h1 class="navbar-brand"><nuxt-link to="/home">Sanya</nuxt-link></h1>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarCollapse"
        aria-controls="navbarCollapse"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarCollapse">
        <ul class="navbar-nav me-auto mb-2 mb-md-0">
          <!-- บริการ -->
          <li>
            <b-dropdown
              variant="link"
              toggle-class="text-decoration-none"
              class="text-teal"
            >
              <template #button-content>
                <span class="text-teal">บริการ</span></template
              >
              <b-dropdown-item href="#" class="item">
                <nuxt-link to="/contract/all" class="disable"
                  >สัญญาสำเร็จรูป</nuxt-link
                >
              </b-dropdown-item>
              <b-dropdown-item href="#"
                >ค้นหาฟรีแลนซ์ด้านกฎหมาย</b-dropdown-item
              >
              <b-dropdown-item href="#" disabled
                >legal encyclopedia <br />
                <sub>(Comming Soon)</sub></b-dropdown-item
              >
            </b-dropdown>
          </li>

          <li class="nav-item">
            <a href="" class="nav-link">ชุมชน</a>
          </li>

          <li class="nav-item">
            <nuxt-link to="/about" class="nav-link">เกี่ยวกับเรา</nuxt-link>
          </li>

          <!--ติดต่อเรา -->
          <li>
            <b-dropdown variant="link" toggle-class="text-decoration-none">
              <template #button-content> ติดต่อเรา </template>
              <b-dropdown-item href="#"
                ><b-icon-inbox></b-icon-inbox> ติดต่อเรา</b-dropdown-item
              >
              <b-dropdown-item href="https://www.facebook.com/" target="_blank"
                ><b-icon-facebook></b-icon-facebook> Facebook</b-dropdown-item
              >
              <b-dropdown-item href="#">
                <b-icon-instagram></b-icon-instagram>
                Instagram</b-dropdown-item
              >
              <b-dropdown-item href="https://www.youtube.com/">
                <b-icon-youtube></b-icon-youtube> Youtube</b-dropdown-item
              >
              <b-dropdown-item href="#">
                <b-icon-linkedin></b-icon-linkedin> Linkedin</b-dropdown-item
              >
              <b-dropdown-item href="#">
                <b-icon-twitter></b-icon-twitter> Twitter</b-dropdown-item
              >
              <b-dropdown-item href="#">
                <b-icon-line></b-icon-line> Line Official</b-dropdown-item
              >
            </b-dropdown>
          </li>

          <!-- ช่วยเหลือ -->
          <li>
            <b-dropdown variant="link" toggle-class="text-decoration-none">
              <template #button-content> ช่วยเหลือ </template>
              <b-dropdown-item href="#"
                >วิธีใช้บริการสัญญาสำเร็จรูป</b-dropdown-item
              >
              <b-dropdown-item href="#"
                >วิธีการใช้บริการฟรีแลนซ์</b-dropdown-item
              >
              <b-dropdown-item href="#">คำถามที่พบบ่อย</b-dropdown-item>
              <b-dropdown-item href="#">คุยกับแอดมิน</b-dropdown-item>
            </b-dropdown>
          </li>

          <li class="nav-item">
            <a href="" class="nav-link">SANYA ACADEMY</a>
          </li>
        </ul>
      </div>
    </div>
    <!-- Right Side -->
    <div class="float-right" id="navbarCollapse">
      <ul class="navbar-nav me-auto mb-2 mb-md-0">
        <li class="nav-item">
          <b-button pill variant="outline-info" style="width: max-content"
            >เข้าสู่ระบบ</b-button
          >
        </li>
        <li class="nav-item" style="width: max-content">
          <div class="nav-link">
            <b-avatar
              src="https://picsum.photos/125/125/?image=40"
              rounded="circle"
            ></b-avatar>
            Username
          </div>
        </li>

        <li class="nav-item">
          <a href="" class="nav-link" style="color: #1d434c"
            ><b-icon-heart></b-icon-heart
          ></a>
        </li>

        <li class="nav-item">
          <a href="" class="nav-link">EN</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {}
</script>

<style scoped>
a.dropdown-item a {
  color: #1d434c;
}
b-dropdown-item {
  background-color: #1d434c;
  color: #04aa6d;
}
b-dropdown:hover .dropdown-item {
  display: block;
  margin-top: 0;
}
nav {
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}
li.nav-item a.navlink {
  color: #1d434c;
}
.btn-link {
  color: #1d434c;
  text-decoration: none;
}
.btn-link:hover {
  color: white;
}
span.text-teal {
  color: #1d434c;
}
li a.nav-link {
  color: #1d434c;
}
.disabled {
  color: lightgrey;
  pointer-events: none;
}

/* Button Login */
.btn:hover {
  background-color: #1d434c;
  color: white;
}
.btn-outline-info {
  color: #1d434c;
  border-color: #1d434c;
}
</style>
