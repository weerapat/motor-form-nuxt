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
            <label for="car-model">Select list:</label>
            <select class="form-control" id="car-model" v-model="user.carModel">
              <option value="" selected>Please select</option>
              <option value="honda">Honda</option>
              <option value="toyota">Toyota</option>
              <option value="bmw">BMW</option>
              <option value="mazda">Mazda</option>
            </select>
          </div>

          <div class="form-group" v-show="user.carModel">
            <label for="desc">Please add detail about your car : {{ user.carModel }}</label>
            <input type="text" class="form-control" id="desc" placeholder="Please enter">
          </div>

          <div class="form-group">
            <label class="radio-inline"><input type="radio" name="optradio" checked>Option 1</label>
            <label class="radio-inline"><input type="radio" name="optradio">Option 2</label>
            <label class="radio-inline"><input type="radio" name="optradio">Option 3</label>
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
export default {
  data() {
    return {
      user: {
        carModel: '',
      }
    }
  }
}
</script>

<style>
  h1 {
    margin-top: 50px;
  }
</style>
