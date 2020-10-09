<template>
  <div class="home">
    <personal/>
    <projects/>
    <skills/>
  </div>
</template>

<script>
// @ is an alias to /src
import personal from "@/components/Home/Personal Info"
import projects from "@/components/Home/Projects List"
import skills from "@/components/Home/Skills List"
export default {
  name: 'Home',
  components: {
    personal,
    projects,
    skills
  }
}
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  h5{
    margin: 0;
  }
  #profile-pic {
    width: 300px;
    border-radius: 100%;
  }
}
</style>