<template>
  <div class="projects_list">
    <h2>My Past Projects</h2>
    <project v-bind:image="'ChromeExtension.png'" v-bind:title="'Custom Chrome Extension'"/>
  </div>
</template>

<script>
import project from "@/components/Home/Project";

export default {
  name: "Projects",
  components: {project},
}
</script>

<style lang="scss" scoped>

</style>