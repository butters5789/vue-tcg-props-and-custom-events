<template>
  <form @submit.prevent="makeActive">
    <div class="mb-3">
      <label for="user-name" class="form-label">Username</label>

      <input
        type="text"
        class="form-control"
        id="user-name"
        v-model="username"
      />
    </div>

    <div class="mb-3">
      <label for="age" class="form-label">Age</label>

      <input
        type="number"
        class="form-control"
        id="age"
        v-model="age"
      />
    </div>

    <button type="submit" class="btn btn-primary mb-3">Activate User</button>
  </form>
</template>

<script>
export default {
  name: 'user-data',
  emits: ['make-user-active'],
  data() {
    return {
      username: '',
      age: 0,
    };
  },
  methods: {
    makeActive() {
      this.$emit('make-user-active', this.username, this.age);
    }
  }
};
</script>
