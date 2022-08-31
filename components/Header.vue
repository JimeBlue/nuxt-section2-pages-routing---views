<!-- How to add the Header component to our pages. -->
<!-- 1) Create the Header.vue component in the component folder.
Add the template with the navbar and the links. -->
<!-- 2) Use the component in the desired page. Next
steps in the main page -->
<template>
  <header class="header">
    <ul class="nav-items">
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/users">Users</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<style scoped>
  .header {
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #ccc;
  }

  .nav-items {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 80%;
  }

  .nav-items a {
    text-decoration: none;
    color: black;
  }

  .nav-items a:hover,
  .nav-items a:active {
    color: white;
  }
</style>

