<template>
  <section class="container">
    <!-- 3) Use the Header component 
    <Header />
    -->
    <nuxt-link to="/users">Users</nuxt-link>
  <button @click="$router.push('/products/')">Go to Products</button>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
/* 4) Import the Header component.
IMPORTANT: notice the tilde slash (~/) in front of
the path in the inport. That comes with nuxt
and it refers to the root folder, so that we 
don´t have to write ..../ 

import Header from '~/components/Header.vue'
*/

export default {
 
  components: {
    Logo,
     /*5) Add the Header component 
    Header
    */
  },

}
</script>

<!-- 6) Now, I have a problem bacause when I go to the
users page the Header disapears, i.e the Header can´t be
seen in all pages. So, what I can do is to add the 
Header component in all the pages I want it to appear.
But that will mean I´ll have to import and register
the Header component in all those pages. So, instead of
using adding it to several pages I can use it in my layout.
And I have to remove it from the main page
Next step in layouts > default.vue-->

<style>

</style>
