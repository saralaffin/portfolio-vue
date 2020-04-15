<template>
  <div class="navbar">
    This is the NavBar component
  </div>
</template>

<script>
export default {
  name: "NavBar",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.navbar {
  background-color: var(--light-blue);
  color: var(--white);
  float: right;
  width: fit-content;
  position: fixed;
  left: 85%;
  top: 50vh;
  transform: rotate(90deg);
  z-index: 1;
}
</style>
