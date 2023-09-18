<template>
  <v-app class="rounded rounded-md">

    <app-bar></app-bar>

    <v-card>
      <v-navigation-drawer v-model="drawer" temporary>
        <v-list-item title="Drawer left"></v-list-item>
        <v-divider />
        <v-list-item title="Information"></v-list-item>
        <v-divider />
        <v-list-item title="Basic"></v-list-item>
      </v-navigation-drawer>
    </v-card>

    <right-panel />

    <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
      <div id="compass" class="compass">
        <img src="/style/compass(1).png" alt="Compass" />
      </div>
      <div id="sphereIdDisplay" class="sphereIdDisplay"></div>

      <div id="root"></div>

      <v-btn color="primary" @click.stop="drawer = !drawer">
        Toggle
      </v-btn>
      Main Content
    </v-main>

  </v-app>
</template>

<script type="module">

import RightPanel from "@/components/RightPanel.vue"
import LeftPanel from "@/components/LeftPanel.vue"
import AppBar from "@/components/AppBar.vue"

// src = "/src/main.tsx"

export default {
  data() {
    return {
      drawer: null,
    }
  },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}


html,
body {
  overflow: hidden;
}

.viewer {
  position: fixed;
  top: 0;
  left: 0;
  outline: none;
}

.sphereIdDisplay {

  position: absolute;
  background-color: rgba(0, 0, 0, 0.7);
  border-radius: 5px;
  top: 200px;
  left: 1100px;
  color: white;
  font-size: 22px;
  pointer-events: none;
  box-shadow: 0 10px 20px 0 rgba(0, 0, 0, 0.2), 0 10px 20px 0 rgba(0, 0, 0, 0.19);
  text-align: center;
}

.compass {
  width: auto;
  height: auto;
  position: absolute;
  background-size: cover;
  transform-origin: center center;
  transition: transform 0.5s ease;
}

span {
  display: grid;
}
</style>