<template>
  <div>
    <!-- Enter the id of the page I want to go to and click the button -->
    <input type="text" v-model="userId">
    <button @click="onLoadUser">Load User</button>
  </div>
</template>

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

