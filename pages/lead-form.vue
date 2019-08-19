<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <a href="/">Go back to homepage</a>
        <h1>Hello new lead form</h1>
        <form>
          <div class="form-group">
            <label for="email">Email address</label>
            <input type="email" class="form-control" id="email" placeholder="Email">
          </div>
          <div class="form-group">
            <label for="exampleInputPassword1">Password</label>
            <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
          </div>
          <div class="form-group">
            <label for="exampleInputFile">File input</label>
            <input type="file" id="exampleInputFile">
            <p class="help-block">Example block-level help text here.</p>
          </div>
          <div class="checkbox">
            <label>
              <input type="checkbox"> Check me out
            </label>
          </div>
          <button type="submit" class="btn btn-success">Submit</button>

          <a href="/package-listing" class="btn btn-danger">Start Compare!!</a>

        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
  }
}
</script>

<style>
  h1 {
    margin-top: 50px;
  }
</style>
