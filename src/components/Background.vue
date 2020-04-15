<template>
  <div id="background">
    <h2>
      I'm a problem solver
    </h2>
    <p>
      I've always been drawn to fixing and creating. As a child, I enjoyed
      building things with my dad. In high school, I fell in love with modular
      origami. <br />
      I studied marine engineering in college, earning my Masters and Bachelors
      from the University of Michigan. I've held a variety of roles in the
      marine engineering field, mainly in the form of internships. <br />
      Next, I tried something more hands-on. 'Sharpened a different saw', if you
      will. I spent 3 seasons with Americorps, mainly on chainsaw crews, out in
      Colorado. <br />
      Now I'm returning to my engineering roots, hopefully with a mix of
      hard-work, hands-on, challenging projects.
    </p>
    <div class="link-container">
      <a href="#skills">Skills</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
#background {
  background-color: var(--dark-blue);
  display: flex;
  flex-direction: column;
  align-items: center;
}
h2 {
  color: var(--white);
}
p {
  text-align: center;
  padding: 1em;
  margin-top: 4vh;
  margin-bottom: 10vh;
}
.link-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
a {
  margin: 0.2em;
}
</style>
