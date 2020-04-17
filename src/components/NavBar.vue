<template>
  <div>
    <div id="debugDiv">{{ debugStr }}</div>
    <div class="navbar">
      <template v-for="section in sections">
        <a
          :key="section"
          :href="'#' + section"
          :class="{ isActive: section === activeSection }"
          >{{ section }}</a
        >
      </template>
      <!-- <a href="#about" :class="{ isActive: 'about' === activeSection }">Intro</a>
    <a href="#background">My Story</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a> -->
      <!-- <p>{{ scrollPosition }}</p>
    <p>{{ activeSection }}</p> -->
    </div>
  </div>
</template>

<script>
// utility copied from https://stackoverflow.com/questions/123999/how-to-tell-if-a-dom-element-is-visible-in-the-current-viewport
function elementInViewport(el) {
  let top = el.offsetTop;
  let height = el.offsetHeight;

  // while (el.offsetParent) {
  //   el = el.offsetParent;
  //   top += el.offsetTop;
  // }

  return (
    top >= window.scrollY && top + height <= window.scrollY + window.innerHeight
  );
}

export default {
  name: "NavBar",
  props: {
    scrollPosition: Number,
  },
  data() {
    return {
      windowHeight: window.innerHeight,
      sections: ["about", "background", "skills", "projects", "contact"],
      activeSection: "try",
    };
  },
  computed: {
    debugStr() {
      let str = "debug";
      const el = document.getElementById("about");

      // // var top = el.offsetTop; //1607
      // // var height = el.offsetHeight; //1254

      // // // while (el.offsetParent) {
      // // //   el = el.offsetParent;
      // // //   top += el.offsetTop;
      // // // }

      // // str =
      // //   top >= window.pageYOffset &&
      // //   top + height <= window.pageYOffset + window.innerHeight;

      str = el.offsetHeight;
      return str;
    },
  },
  created() {
    document.addEventListener("scroll", this.handleScroll);
  },
  // destroyed() {
  //   document.removeEventListener("scroll", this.handleScroll);
  // },
  methods: {
    handleScroll() {
      // console.log(window.scrollY);
      let vx = this;
      vx.sections.find((section) => {
        const el = document.getElementById(section);
        if (elementInViewport(el)) {
          vx.activeSection = section;
        }
      });
    },
  },
};
</script>

<style scoped>
#debugDiv {
  position: fixed;
}
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  transform: translate(45vw, 50vh) rotate(90deg);
  z-index: 1;
}
a:first-child {
  background-color: red;
}
a:nth-child(2) {
  background-color: orangered;
}
a:nth-child(3) {
  background-color: green;
}
a:nth-child(4) {
  background-color: blue;
}
a:nth-child(5) {
  background-color: blueviolet;
}
a {
  padding: 0.2em;
  opacity: 60%;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.isActive {
  opacity: 100%;
  padding-bottom: 0.5em;
}
</style>
