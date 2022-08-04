<template>
  <div class="form-group text-center">
    <p class="" style="margin-top: 25px">
      <!-- Previous Page -->
      <nuxt-link :to="`/contract/create/step/${page - 1}`">
        <b-icon-arrow-left-circle-fill
          style="cursor: pointer; font-size: 22px"
        ></b-icon-arrow-left-circle-fill>
      </nuxt-link>
      &nbsp; หน้า {{ page }}/7 &nbsp;
      <!-- Next Page -->
      <nuxt-link :to="`/contract/create/step/${page + 1}`">
        <b-icon-arrow-right-circle-fill
          style="cursor: pointer; font-size: 22px"
        ></b-icon-arrow-right-circle-fill>
      </nuxt-link>
    </p>
  </div>
</template>
<script>
export default {
  name: 'Step',
  props: ['page'],
}
</script>
