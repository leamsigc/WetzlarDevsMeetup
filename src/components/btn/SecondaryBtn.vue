<template>
  <a href="#" class="btn btn-secondary">{{ textContent }}</a>
</template>

<script>
export default {
  name: "SecondaryBtn",
  props: {
    textContent: {
      type: String,
      default: null
    }
  }
};
</script>

<style></style>
