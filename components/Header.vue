<template>
  <div>
    <!-- <div class="topnav">
      <a class="active" href="#home">Home Logo</a>
      <a href="#news">ชุมชน</a>
      <a href="#news">เกี่ยวกับเรา</a>
      <a href="#news">ติดต่อเรา</a>
      <a href="#news">ช่วยเหลือ</a>
      <a href="#news">SANYA ACADEMY</a>
      <a href="#contact">Contact</a>
      <a href="#about">About</a>
      <div class="split">
        <a href="#about">เข้าสู่ระบบ</a>
        <a href="">TH</a> | <a href="">EN</a>
      </div>
    </div> -->
    <!-- Fixed navbar -->
    <nav
      class="navbar navbar-expand-md navbar-light bg-light text-darkgreen fixed-top"
      id="NAV"
    >
      <div class="container-fluid">
        <h1 class="navbar-brand text-darkgreen" to="/">
          <a href="/"></a> Sanya
        </h1>
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
            <li class="nav-item active">
              <a class="nav-link" href="http://localhost:8000/login">Admin</a>
            </li>
            <li>
              <b-dropdown variant="link" class="dropdown">
                <template #button-content>
                  <span class="text-teal">บริการ</span></template
                >
                <b-dropdown-item href="#">สัญญาสำเร็จรูป</b-dropdown-item>
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
              <a href="" class="nav-link">เกี่ยวกับเรา</a>
            </li>

            <li>
              <b-dropdown variant="link">
                <template #button-content> ติดต่อเรา </template>
                <b-dropdown-item href="#"
                  ><b-icon-inbox></b-icon-inbox> ติดต่อเรา</b-dropdown-item
                >
                <b-dropdown-item href="#"
                  ><b-icon-facebook></b-icon-facebook> Facebook</b-dropdown-item
                >
                <b-dropdown-item href="#">
                  <b-icon-instagram></b-icon-instagram>
                  Instagram</b-dropdown-item
                >
                <b-dropdown-item href="#">
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

            <li>
              <b-dropdown variant="link">
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
            <a href="" class="nav-link"><b-icon-heart></b-icon-heart></a>
          </li>

          <li class="nav-item">
            <a href="" class="nav-link">EN</a>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
/* Add a black background color to the top navigation */
.topnav {
  background-color: white;
  overflow: hidden;
  text-align: center;
}

/* Style the links inside the navigation bar */
.topnav a {
  float: left;
  /* color: #f2f2f2; */
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

/* Change the color of links on hover */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}

/* Add a color to the active/current link */
.topnav a.active {
  background-color: #04aa6d;
  color: white;
}
.topnav .split {
  float: right;
}

b-dropdown b-dropdown-item:hover {
  background-color: #1d434c;
}
</style>
