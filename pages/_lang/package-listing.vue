<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <h1 class="title">Packages</h1>

        <div class="panel panel-success"
          v-for="(carPackage, index) in carPackages"
        >
          <div class="panel-heading">
            <h3 class="panel-title">{{ carPackage.name }}</h3>

          </div>
          <div class="panel-body">
            <a  href="/checkout"
              class="btn btn-success pull-right">Buy
            </a>
            <div>Price: {{ carPackage.price }}</div>
            <div>Deduct: {{ carPackage.deductible_amount }}</div>
            <div>Total price: {{ carPackage.price - carPackage.deductible_amount }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
  },
  data() {
    return {
      carPackages: [
        {
          name: 'Viriyah',
          price: 10000,
          deductible_amount: 1000,
        },
        {
          name: 'GG Motor  Gen X',
          price: 20000,
          deductible_amount: 1000,
        }
      ]
    }

  }
}
</script>

<style>
  .title {
    margin-top: 50px;
  }
</style>
