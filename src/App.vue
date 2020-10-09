<template>
  <div id="app">
    <div id="nav">
      <div style="padding: 5px 0; display: flex; width: 100%; justify-content: space-between">
        <h2 style=" margin: 0">Welcome</h2>
        <button v-on:click="shownav" v-if="shown">X</button>
        <button v-on:click="shownav" v-else>=</button>
      </div>
      <transition name="jumpdown">
        <div id="hidenav" v-if="shown">
          <router-link class="nav-item" to="/">Home</router-link>
          <router-link class="nav-item" to="/contact">Contact</router-link>
        </div>
      </transition>
    </div>
    <router-view style="margin-top: 5px"/>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      shown: false
    }
  },
  methods: {
    shownav() {
      this.shown = !this.shown;
    }
  },
}

</script>

<style lang="scss">
.jumpdown-enter-active, .jumpdown-leave-active {
  transition: opacity 0.25s ease-out;
}

.jumpdown-enter, .jumpdown-leave-to {
  opacity: 0;
}

#nav {
  display: flex;
  flex-direction: column;
  text-align: center;
  background-color: black;
  color: white;
  padding: 10px 15px 15px 15px;

  #hidenav{
    display: flex;
    flex-direction: column;
    text-align: center;
    .nav-item {
      padding: 7px 0;
      width: 100%;
    }
    padding-bottom: 10px;
  }
}
button{
  background-color: transparent;
  color: white;
  text-align: center;
  width: 30px;
  height: 30px;
  border: solid 1px white;
  border-radius: 5px;
}

a {
  text-decoration: none;
  color: inherit;
  &:hover {
    color: rgba(white, 0.5);
    text-decoration: none;
  }

  &:visited {
    text-decoration: none;
    color: inherit;
  }
}
</style>
