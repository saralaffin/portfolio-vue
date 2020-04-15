<template>
  <div id="projects">
    <h2>
      Recent Projects
    </h2>
    <project
      id="pawsitivity"
      description="First try!"
      githubURL="#"
      deployedURL="#"
    />
  </div>
</template>

<script>
import Project from "./Project.vue";
export default {
  name: "Projects",
  props: {
    msg: String,
  },
  components: {
    Project,
  },
};
</script>

<style scoped>
#projects {
  background-color: var(--dark-blue);
  display: flex;
  flex-direction: column;
  align-items: center;
}
h2 {
  color: var(--white);
  opacity: 1;
}
#pawsitivity {
  background-image: url("../assets/pawsitivity.png");
}
</style>
