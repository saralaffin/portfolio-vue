<template>
  <div class="sub-skills">
    <!-- <p>{{ icon }}</p> -->
    <h4>
      {{ title }}
    </h4>
    <p>{{ content }}</p>
  </div>
</template>

<script>
export default {
  name: "SubSkills",
  props: {
    title: String,
    content: String,
    icon: String,
  },
};
</script>

<style scoped>
.sub-skills {
  background-color: var(--white);
  display: flex;
  flex-direction: column;
  align-items: center;
}
h2 {
  color: var(--dark-blue);
}
</style>
