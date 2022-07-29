<template>
  <div class="app">
    <Header />
    <nuxt id="nuxt-content" />
    <Footer />
  </div>
</template>
<script></script>

<style>
.app {
  font-family: 'Mitr',sans-serif;

  min-height: 100vh;

  display: grid;
  grid-template-rows: 1fr auto;
}

#nuxt-content {
  margin-top: 6.5rem;
}
</style>
