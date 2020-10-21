<template>
  <div class="home" :style="color">
    <personal/>
    <projects/>
    <skills/>
    <div class="scroll"></div>
    <!--education/-->
    <!--experience/-->
  </div>
</template>

<script>
// @ is an alias to /src
import personal from "@/components/Home/Personal Info"
import projects from "@/components/Home/Projects List"
import skills from "@/components/Home/Skills List"
import education from "@/components/Home/Educations List"
import experience from "@/components/Home/Experiences List"

export default {
  name: 'Home',
  components: {
    personal,
    projects,
    skills,
    education,
    experience
  },
  data() {
    return {
      color:null
    }
  },
  mounted() {
    window.addEventListener('scroll', this.chcolor);
  },
  destroy() {
    window.removeEventListener('scroll', this.chcolor)
  },
  methods: {
    chcolor() {
      let str = 'let y = (window.scrollY || window.pageYOffset) / window.outerHeight\
      y = 1- y\
      this.color = `background-color: rgba(69,111,225, ${y});`;\
      console.log(y)'
      this.color = `background-color: white);`;
    }
  },
  created() {
    this.chcolor()
  }
}
</script>

<style lang="scss" scoped>

.home {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-top: 0 !important;


  .scroll{
    width: 100vw;
    height: 100vh;
  }

  h5 {
    margin: 0;
  }

  * {
    margin-bottom: 40px;
    width: 100%;
  }
}
</style>