<template>
  <!-- Welcome Homepage -->
  <div class="">
    <Header />
    <!-- Jumbotron -->
    <div class="p-5 bg-info text-white" style="margin-top: 58px">
      <h1 class="mb-3">ฟรี</h1>
      <h2 class="mb-3">บริการสร้าง "สัญญา" ด้วยตนเอง</h2>
      <h4>> เลือก "สัญญา" ที่คุณต้องการ</h4>
      <h4>> ตอบคำถาม (กรอกข้อมูลในสัญญา)</h4>
      <h4>> ส่ง Invitation link สู่คู่สัญญา</h4>
      <h4>> เซ็นทั้งสองฝ่าย</h4>
      <h5 class="text-danger">
        หมายเหตุ สามารถปรึกษาความถูกต้องของสัญญา กับสัญญาได้เพิ่มเติม*
      </h5>
      <a class="btn btn-primary bg-dark" href="" role="button">Click</a>
    </div>
    <!-- Jumbotron -->

    <div>
      <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="1024"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
        <!-- Text slides with image -->
        <b-carousel-slide
          caption="First slide"
          text="Nulla vitae elit libero, a pharetra augue mollis interdum."
          img-src="https://picsum.photos/1024/480/?image=52"
        ></b-carousel-slide>

        <!-- Slides with custom text -->
        <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
          <h1>Hello world!</h1>
        </b-carousel-slide>

        <!-- Slides with image only -->
        <b-carousel-slide
          img-src="https://picsum.photos/1024/480/?image=58"
        ></b-carousel-slide>

        <!-- Slides with img slot -->
        <!-- Note the classes .d-block and .img-fluid to prevent browser default image alignment -->
        <b-carousel-slide>
          <template #img>
            <img
              class="d-block img-fluid w-100"
              width="1024"
              height="480"
              src="https://picsum.photos/1024/480/?image=55"
              alt="image slot"
            />
          </template>
        </b-carousel-slide>

        <!-- Slide with blank fluid image to maintain slide aspect ratio -->
        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse
            eros felis, tincidunt a tincidunt eget, convallis vel est. Ut
            pellentesque ut lacus vel interdum.
          </p>
        </b-carousel-slide>
      </b-carousel>

      <p class="mt-4">
        Slide #: {{ slide }}<br />
        Sliding: {{ sliding }}
      </p>
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
export default {
  name: 'HomePage',
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      slide: 0,
      sliding: null,
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
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
