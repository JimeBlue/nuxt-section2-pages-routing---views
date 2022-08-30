<template>
  <section class="container">
    <!-- Create link -->
    <nuxt-link to="/users">Users</nuxt-link>
    <!-- 2) Add a button to navigate programatically to /products -->
  <button @click="$router.push('/products/')">Go to Products</button>
  </section>
</template>

<!-- CHALLENGE: 
1) Create two routes: /products and /producsts:pid
2) Add a button to the main page. The buttons should
navigate programatically to /products
3) Add two links to the /products page. These links should
go to /products/1 and /products/2
4) Output the product id in the producsts:pid page
-->

<!-- SOLUTION: 
1) Inside the pages folder, create the products folder and inside it 
the index.vue file. This represents the first route. The inside the 
products folder create the _pid folder and inside it the index.vue file.
This represents the second route.
  -->
<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },

}
</script>

<style>
.container
{
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links
{
  padding-top: 15px;
}
</style>
