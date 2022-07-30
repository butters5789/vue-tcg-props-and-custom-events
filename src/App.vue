<template>
  <div class="container">
    <user-data @make-user-active="activateUser" />
    <active-user :username="activeUsername" :age="activeAge" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeUsername: '',
      activeAge: 0,
    };
  },
  methods: {
    activateUser(username, age) {
      this.activeUsername = username;
      this.activeAge = age;
    }
  }
};
</script>

<style></style>
