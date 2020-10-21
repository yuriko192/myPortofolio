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
      return `width: ${this.rating}%; background: ${this.color};`;
    }
  },
}
</script>

<style lang="scss" scoped>
.skill {
  margin: 20px 0;
  display: flex;
  justify-content: space-between;
  text-align: center;
  padding: 0 10px;

  .head {
    font-size: large;
    width: max(100px);
  }

  .rate_cont {
    display: flex;
    width: calc(100% - 100px);
    margin: auto;
    justify-content: center;

    .rate {
      width: calc(100% - 100px);
      height: 20px;
      border: solid 3px black;
      border-radius: 10px;
      margin: auto 20px;
      background: #2f2f2f;

      .ratebar {
        height: 100%;
        border-radius: inherit;
      }
    }

    .percent {
      align-self: flex-end;
    }
  }

}
</style>