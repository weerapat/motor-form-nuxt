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
            <NuxtLink to="/checkout" class="btn btn-success pull-right">Buy</NuxtLink>
            <div>Price: {{ carPackage.price }}</div>
            <div>Deduct: {{ carPackage.deductible_amount }}</div>
            <div>Total price: {{ carPackage.price - carPackage.deductible_amount }}</div>
          </div>
        </div>

<!--        <input v-model="search" type="text">-->

        <div class="form-group">
          <label for="search">Search</label>
          <input v-model="search" type="text" class="form-control" id="search" placeholder="Search post">
        </div>

        <div class="panel panel-danger"
          v-for="post in filteredPosts"
        >
          <div class="panel-heading">
            <h3 class="panel-title">{{ post.title }}</h3>
          </div>
          <div class="panel-body">
            <p>{{ post.body }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.$axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(res => {
        this.posts = res.data;
      });
  },

  data() {
    return {
      posts: [],
      search: '',
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
  },

  computed: {
    filteredPosts() {
      return this.posts.filter((post) => {
        return post.title.match(this.search);
      })
    }
  }
}
</script>

<style>
  .title {
    margin-top: 50px;
  }
</style>
