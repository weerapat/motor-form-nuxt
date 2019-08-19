<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6 col-md-offset-3">
        <a href="/">Go back to homepage</a>
        <h1>Hello checkout form</h1>
        <form>
          <div class="form-group">
            <label for="email">Email address</label>
            <input type="email" class="form-control" id="email" placeholder="Email">
          </div>
          <div class="form-group">
            <label for="exampleInputPassword1">Password</label>
            <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style>
  h1 {
    margin-top: 50px;
  }
</style>
