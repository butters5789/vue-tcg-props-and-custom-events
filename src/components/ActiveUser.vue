<template>
  <div class="card md-3" style="width: 18rem">
    <div class="card-body">
      <h5 class="card-title">{{ username }}</h5>
      <h6 class="card-subtitle mb-2 text-muted">{{ age }}</h6>
    </div>
  </div>
</template>

<script>
export default {
  name: 'active-user',
  props: {
    username: {
      type: String,
      required: true,
    },
    age: {
      type: Number,
      required: true,
    },
  },
};
</script>

<style></style>
