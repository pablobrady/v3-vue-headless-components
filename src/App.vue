<template>
  <img class="mx-auto" width="100" height="100" alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="HELLO V3 WORLD!" />

  <div class="m-4 p-3">
    <EnableNotifications />
  </div>

  <div class="m-4 p-3">
    <ToggleNewsletters />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import EnableNotifications from './components/EnableNotifications.vue'
import ToggleNewsletters from './components/ToggleNewsletters.vue'

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld,
    EnableNotifications,
    ToggleNewsletters
  },
  data() {
    return {
      users: [
        {
          name: "John",
          age: 35,
          favorite: false,
        },
        {
          name: "Jane",
          age: 30,
          favorite: true,
        },
      ]
    }
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
