<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12 text-center">
        <logo />
        <h1 class="title">
          motor-form-nuxt
        </h1>
        <h2 class="subtitle">
          New motor form
        </h2>
        <div class="links">
          <NuxtLink
            to="/lead-form"
            class="button--green"
          >
            Go to new motor lead form
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
