<template>
  <div id="contact">
    <h2>
      Keep in touch!
    </h2>
    <p>I'm looking for full time work</p>
    <a href="https://www.linkedin.com/in/saralaffin">linkedIn</a>
    <a href="https://github.com/saralaffin">github</a>
  </div>
</template>

<script>
export default {
  name: "Contact",
};
</script>

<style scoped>
#contact {
  background-color: var(--white);
  display: flex;
  flex-direction: column;
  align-items: center;
}
h2 {
  color: var(--dark-blue);
}
</style>
