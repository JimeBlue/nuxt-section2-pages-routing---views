<template>
  <!-- Create a route with a dynamic path -->
  <h1>A single user, with ID: {{  $route.params.id  }}</h1>
</template>

<script>
export default {
  /* Validating parameters so that not anything we enter
  after /users leads to that route. For example, if our
  id are numbers, so entering /users/whatever shouldn´t
  go to that page  */

  /* 1) Use the validate property, which is a method, 
  where we can get some argument. Let´s name that
  argument data */
  validate(data) {
    console.log(data)
    /* 2) Now that we have access to the argument of the
    validate method, we can check if the parameter is
    equal to 1. Note: use doble equal signs, otherwise
    the data type won´t match, ´cause in the browser the
    parameter is a string and here a number. If I enter
    /users/1, it works and if I enter /users/50 it doesn´t
    work
    
    return data.params.id == 1
    
    */ 
    
    /* 3) Using regex, we can check if the id is a number.
    So, if I enter /users/50 or /users/1, it works. But
    if I enter something that is not a number, like 
    /users/whatever, it doesn´t work and I get
    the "this page could not be found" page*/
    return /^\d+$/.test(data.params.id)
  }
}
</script>