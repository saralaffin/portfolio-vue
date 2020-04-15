<template>
  <div class="project">
    <p>
      {{ description }}
    </p>
    <div class="link-container">
      <a :href="githubURL">GitHub</a>
      <a :href="deployedURL">
        Deployed
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: {
    description: String,
    githubURL: String,
    deployedURL: String,
  },
};
</script>

<style scoped>
.project {
  background-color: var(--beige);
  display: flex;
  flex-direction: column;
  align-items: center;
}
h2 {
  color: var(--white);
  opacity: 1;
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
