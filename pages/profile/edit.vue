<template>
  <!-- Welcome -->
  <div class="text-center">
    <!-- Jumbotron -->
    <div class="p-5 text-center bg-primary" >
      <b-img
        src="https://picsum.photos/125/125/?image=58"
        rounded="circle"
      ></b-img>
      <!-- <a class="btn btn-primary" href="" role="button">Call to action</a> -->
    </div>
    <!-- Jumbotron -->

    <!-- Bio -->
    <div class="container text-center">
      <h4>แก้ไขโปรไฟล์</h4>
    </div>

    <div class="col-sm-8 offset-sm-2">
      <b-form @submit="onSubmit" @reset="onReset" v-if="show">
        <b-form-group
          id="input-group-1"
          label="Email address:"
          label-for="input-1"
          description="We'll never share your email with anyone else."
        >
          <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            placeholder="Enter email"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.name"
            placeholder="Enter name"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-3" label="gender:" label-for="input-3">
          <b-form-select
            id="input-3"
            v-model="form.gender"
            :options="gender"
            required
          ></b-form-select>
          <!-- <v-date-picker v-model="date"  />
          <v-date-picker v-model="date" :masks="masks" ref="picker" /> -->
        </b-form-group>

        <b-form-group id="input-group-4" v-slot="{ ariaDescribedby }">
          <b-form-checkbox-group
            v-model="form.checked"
            id="checkboxes-4"
            :aria-describedby="ariaDescribedby"
          >
            <b-form-checkbox value="me">Check me out</b-form-checkbox>
            <b-form-checkbox value="that">Check that out</b-form-checkbox>
          </b-form-checkbox-group>
        </b-form-group>

        <b-button type="submit" variant="primary">Submit</b-button>
        <b-button type="reset" variant="danger">Reset</b-button>
      </b-form>

      <b-card class="mt-3" header="Form Data Result">
        <pre class="m-0">{{ form }}</pre>
      </b-card>
    </div>
  </div>
</template>

<script>
import Footer from '~/components/Footer.vue'
import Header from '~/components/Header.vue'
const mask = 'YYYY-MM-DD'
export default {
  name: 'Profile',
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      form: {
        email: '',
        name: '',
        gender: null,
        checked: [],
      },
      gender: ['ชาย', 'หญิง'],
      show: true,
      date: new Date(),
      masks: {
        input: mask,
      },
    }
  },
  methods: {
    onSubmit(event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    },
    onReset(event) {
      event.preventDefault()
      // Reset our form values
      this.form.email = ''
      this.form.name = ''
      this.form.food = null
      this.form.checked = []
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    },
  },
}
</script>
<style scoped>
/* Write Css */
</style>
