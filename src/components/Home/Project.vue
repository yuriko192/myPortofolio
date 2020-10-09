<template>
  <div class="project">
    <img :src="require('@/assets/'+image)" alt="">
    <h3>{{ title }}</h3>
  </div>
</template>

<script>
export default {
  name: "project",
  props:["image", "title"],
}
</script>

<style scoped lang="scss">
.project {
  margin: 10px 0;
  img {
    width: 300px;
  }
}

</style>