<template>
  <div class="skills_list">
    <h2>My Skills</h2>
    <skill v-bind:head="'Java'" v-bind:rating="'50'" v-bind:color="'#42b983'"/>
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
  margin-bottom: 20px;
}
</style>