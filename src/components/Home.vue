<script setup>
import Introduction from './Introduction.vue'
import Deconstruction from './Deconstruction.vue'
import Work from './Work.vue'
import School from './School.vue'
import Music from './Music.vue'
</script>

<template>
  <header class="nav-bar">
    <nav>
      <div class="nav-items">
        <a v-bind:style="[visible[0] === 1 ? 'color: green;' : '']" @click="showIntroduction">Intro</a>
        <a v-bind:style="[visible[1] === 1 ? 'color: green;' : '']" @click="showDeconstruction">Deconstruction</a>
        <a v-bind:style="[visible[2] === 1 ? 'color: green;' : '']" @click="showWork">Work</a>
        <a v-bind:style="[visible[3] === 1 ? 'color: green;' : '']" @click="showSchool">School</a>
        <a v-bind:style="[visible[4] === 1 ? 'color: green;' : '']" @click="showMusic">Music</a>
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
  <div id="parent" v-if="visible[3] === 1">
    <School />
  </div>
  <div id="parent" v-if="visible[4] === 1">
    <Music />
  </div>
  <div>
    <p id="code-blurb">Wanna see the code for this website? <a id="code-link"
        href="https://github.com/nhanzel/MyStory">check it out</a>
    </p>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      visible: [1, 0, 0, 0, 0] //home, deconstruction, work, school, music
    };
  },
  methods: {
    showIntroduction() {
      this.visible = [1, 0, 0, 0, 0];
    },
    showDeconstruction() {
      this.visible = [0, 1, 0, 0, 0];
    },
    showWork() {
      this.visible = [0, 0, 1, 0, 0];
    },
    showSchool() {
      this.visible = [0, 0, 0, 1, 0];
    },
    showMusic() {
      this.visible = [0, 0, 0, 0, 1];
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

.nav-items>a {
  color: ghostwhite;
  text-decoration: none;
  font-weight: 500;
  font-size: 16px;
  transition: .4s ease-in-out;
}

.nav-items>a:hover {
  text-decoration: underline;
}

nav {
  width: 100%;
  max-width: 1100px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#code-blurb {
  position: fixed;
  bottom: 2%;
  right: 2%;
  font-size: 14px;
  color: rgb(211, 211, 211, .5);
}

#code-link {
  color: rgb(34, 139, 34, .5);
}
</style>