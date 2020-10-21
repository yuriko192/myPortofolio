<template>
  <div class="personal">
    <img id="profile-pic"
         src="https://avatars2.githubusercontent.com/u/30367416?s=460&u=237d28568e566fc4f387769974135345aa45eabc&v=4">
    <h1>Ivan Wijaya</h1>
    <h5>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean eros lorem, euismod eget accumsan nec</h5>
  </div>
</template>

<script>
export default {
  name: "Personal_Info"
}
</script>

<style lang="scss" scoped>
.personal {
  padding-top: 5px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  background-image: linear-gradient(#366c92 0%, #45afd9 10%, rgba(black,0) 100%);

  h5 {
    margin: 0;
  }

  #profile-pic {
    width: 200px;
    border-radius: 100%;
  }
}

</style>