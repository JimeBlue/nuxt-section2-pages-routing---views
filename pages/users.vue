<!-- EXPLANATION:  Creating nested routes: it´s not about 
nested folders which crated a specific parameter, 
like users > _id that we´ll create /users/10. 
It´s about displaying the content of a route inside a page/pages.
In this case, in the /users page I want to show
a input field to enter an id and a button. When the user
clicks the button the single user page with the entered 
id should be displayed below the input and the button.-->

<!-- 1) Create a file next to the folder where you want 
to create the nested route. The file must have the same
name as the folder. In this case I create the file
users.vue next to the foler users -->

<!-- 2) Add a template in the newly created users.vue file.
That template will be now a wrapper for both the index.vue inside
the users folder and for any page inside the _id folder, also
inside the users folder  -->

<template>
  <div>
<!-- 3) Now, I want the input and the button to appear in
/users and also in any other /users with parameters, like
users/2. To do that, here in users.vue I put the input and
the button -->
    <input type="text" v-model="userId">
    <button @click="onLoadUser">Load User</button>
    <!-- 5) Add the <nuxt-child /> component, which marks
    where the different sections of the nested route should 
    loaded. In this example, we have 2 sections. /users, 
    represented by users > index.vue and users/1 or
    users/2 represented by the index.vue inside _id.
    The next step is in users > index.vue
 -->
    <nuxt-child />
  </div>
</template>

<!-- 4) Add the necessary data and methods in the script section -->
<script>
export default {
  data() {
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser() {
      // Navigate programatically
      this.$router.push('/users/' + this.userId)
    }
  }
}
</script>