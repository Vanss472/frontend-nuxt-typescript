<template>
  <div class="menu">
    <p class="menu-title">Aye wench jolly boat lass</p>
    <div class="menu-group-buttons">
      <button type="button" @click="toggleBtnOne">
        Wench Letter of Marque
      </button>
      <button type="button" @click="toggleBtnTwo">Barbary Coast provost</button>
    </div>
  </div>
</template>

<script lang="ts">
import Vue, { PropOptions } from 'vue'

export default Vue.extend({
  name: 'Menu',
  props: {
    toggleBtnOne: {
      type: Function,
      required: true,
      default: () => false,
    },
    toggleBtnTwo: {
      type: Function,
      required: true,
      default: () => false,
    },
  },
})
</script>

<style scoped>
.menu {
  padding-right: 1.25rem;
  padding-left: 1.25rem;
  margin-top: 1rem;
}
.menu-title {
  text-transform: uppercase;
  color: white;
  font-size: 1rem;
  font-weight: bold;
  letter-spacing: -1px;
}
.menu-group-buttons {
  display: flex;
  flex-direction: column;
  margin-top: 2rem;
}
.menu-group-buttons button {
  border: 1px solid white;
  margin: 0;
  padding: 0;
  border-radius: 0;
  background: transparent;
  appearance: none;
  text-decoration: none;
  display: flex;
  padding-top: 1rem;
  padding-bottom: 1rem;
  padding-right: 2rem;
  padding-left: 2rem;
  color: white;
  cursor: pointer;
  font-size: 1rem;
}
.menu-group-buttons button:hover {
  color: black;
  background-color: white;
}
.menu-group-buttons button:not(:first-child) {
  margin-top: 2rem;
}
@media only screen and (min-width: 768px) {
  .menu {
    flex-grow: 1;
    margin-top: 0rem;
  }
  .menu-group-buttons {
    flex-direction: row;
  }
  .menu-group-buttons button:not(:first-child) {
    margin-top: 0;
  }
  .menu-group-buttons button:not(:last-child) {
    margin-right: 2rem;
  }
}
</style>
