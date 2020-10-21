<template>
  <div class="skills_list">
    <h2>My Skills</h2>
    <skill v-bind:head="'Web Development'" v-bind:rating="'90'" v-bind:color="'#49dba8'"/>
    <skill v-bind:head="'C++'" v-bind:rating="'90'" v-bind:color="'#4da8db'"/>
    <skill v-bind:head="'Java'" v-bind:rating="'90'" v-bind:color="'#b94242'"/>
    <skill v-bind:head="'C#'" v-bind:rating="'70'" v-bind:color="'#4a42b9'"/>
    <skill v-bind:head="'Flutter'" v-bind:rating="'70'" v-bind:color="'#4264b9'"/>
    <skill v-bind:head="'Rust'" v-bind:rating="'60'" v-bind:color="'#ababab'"/>
    <skill v-bind:head="'Go'" v-bind:rating="'60'" v-bind:color="'#42b9b9'"/>
  </div>
</template>

<script>
import skill from "@/components/Home/Skill"
export default {
name: "Skills",
  components:{
  skill
  }
}
</script>

<style lang="scss" scoped>
.skills_list{
  display: flex;
  flex-direction: column;
  width: 100%;
  margin-bottom: 20px;
}
</style>