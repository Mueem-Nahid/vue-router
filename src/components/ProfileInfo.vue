<template>
  <div>
    <h2>This is Profile info page</h2>
    <h4>User name: {{user}}</h4>
    <button @click="Back">Back</button>
  </div>
</template>

<script>
export default {
  name: "ProfileInfo",
  data() {
    return {
      user: this.$route.params.user,
    };
  },
  methods: {
    updateUser() {
      this.user = this.$route.params.user
    },
    Back() {
      this.$router.go(-1)
    }
  },
  watch: {
    $route: 'updateUser'
  }
};
</script>