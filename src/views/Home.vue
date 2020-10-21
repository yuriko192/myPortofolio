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
      let y = 1 + (window.scrollY || window.pageYOffset) / 150
      y = y < 1 ? 1 : y // ensure y is always >= 1 (due to Safari's elastic scroll)
      const [r, g, b] = [69/y, 111/y, 225/(y/2)].map(Math.round)
      this.color = `background-color: rgb(${r}, ${g}, ${b});`;
      if ((r+g+b)/3 < 70){
        this.color+= `color: white;`
      }
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

  #profile-pic {
    width: 300px;
    border-radius: 100%;
  }

  * {
    margin-bottom: 40px;
  }
}
</style>