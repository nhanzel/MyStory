<script setup>
  import Introduction from './Introduction.vue'
  import Deconstruction from './Deconstruction.vue'
  import Work from './Work.vue'
</script>

<template>
    <header class="nav-bar">
      <nav>
        <div class="nav-items">
          <a v-bind:style="[visible[0] === 1 ? 'color: green;' : '']" @click="showIntroduction">Intro</a>
          <a v-bind:style="[visible[1] === 1 ? 'color: green;' : '']" @click="showDeconstruction">Deconstruction</a>
          <a v-bind:style="[visible[2] === 1 ? 'color: green;' : '']" @click="showWork">Work</a>
        </div>
      </nav>
    </header>
    <div id="parent" v-if="visible[0] === 1">
      <Introduction />
    </div>
    <div id="parent" v-if="visible[1] === 1">
      <Deconstruction />
    </div>
    <div id="parent" v-if="visible[2] === 1">
      <Work />
    </div>
</template>
  
<script>
  export default {
    name: 'app',
    data() {
      return {
        visible: [1,0,0] //home, deconstruction, work
      };
    },
    methods: {
      showIntroduction() {
        this.visible = [1,0,0];
      },
      showDeconstruction() {
        this.visible = [0,1,0];
      },
      showWork() {
        this.visible = [0,0,1];
      },
    },
  }
</script>
  
<style scoped>
.nav-bar {
    position: fixed;
    top: 0;
    left: 0;
    padding: 0 15px;
    height: 60px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.nav-items {
    display: flex;
    gap: 40px;
}
.nav-items > a {
    color: ghostwhite;
    text-decoration: none;
    font-weight: 500;
    font-size: 16px;
    transition: .4s ease-in-out;
}
.nav-items > a:hover {
    text-decoration: underline;
}
nav {
    width: 100%;
    max-width: 1100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>
  