<template>
  <div class="skill">
    <span class="head">{{ head }}</span>
    <div class="rate_cont">
      <div class="rate">
        <div class="ratebar" :style="styling"></div>
      </div>
      <span class="percent">{{ rating }}%</span>
    </div>

  </div>
</template>

<script>
export default {
  name: "Skill",
  props: ["head", "rating", "color"],
  computed: {
    styling() {
      return "width: " + this.rating + "%; " +
          "background-color: " + this.color + ";";
    }
  },
}
</script>

<style lang="scss" scoped>
.skill {
  display: flex;
  justify-content: space-between;
  width: 300px;

  .head {
    font-size: large;
  }

  .rate_cont {
    display: flex;
    width: 200px;
    justify-content: space-between;

    .rate {
      width: 150px;
      height: 20px;
      border: solid 1px black;
      border-radius: 10px;

      .ratebar {
        height: 100%;
        border-radius: inherit;
      }
    }

    .percent {
      align-self: flex-end;
      margin: auto 0;
    }
  }

}
</style>