<template>
  <div class="header">
    <h1>SARA LAFFIN</h1>
    <a href="#about">Meet your company's next software engineer!</a>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.header {
  background-image: url("../assets/mesaverde.jpg");
  height: 100vh;
  width: 100vw;
  background-position: center;
  background-size: cover;
  display: flex;
  flex-direction: column;
  align-items: center;
}
h1 {
  font-size: 6vh;
  font-family: "Catamaran", sans-serif;
  color: white;
  opacity: 0.85;
  margin-top: 15vh;
  margin-bottom: 40vh;
}
a {
  color: white;
  padding: 1.2em;
  background: #4679a6;
  text-decoration: none;
  border-radius: 0.5em;
  text-align: center;
  max-width: 80vw;
  opacity: 0.85;
}
@media only screen and (min-width: 780px) {
  h1 {
    font-size: 10vh;
    margin-top: 11vh;
  }
}
</style>
