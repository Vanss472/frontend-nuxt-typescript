<template>
  <div>
    <div class="container">
      <div class="content">
        <Logo />
        <Hero />
        <Menu :toggle-btn-one="toggleBtnOne" :toggle-btn-two="toggleBtnTwo" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Menu from '~/components/Menu.vue'

export default Vue.extend({
  components: {
    Menu,
  },
  data() {
    return {
      showBtnOne: false,
      showBtnTwo: false,
    }
  },
  methods: {
    toggleBtnOne() {
      console.log('clicked 1')
      this.showBtnOne = !this.showBtnOne
    },
    toggleBtnTwo() {
      console.log('clicked 2')
      this.showBtnTwo = !this.showBtnTwo
    },
  },
})
</script>

<style>
.container {
  position: relative;
  width: 100%;
  height: 100vh;
  background-image: url('https://picsum.photos/1920/900?grayscale&random=1');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}

.content {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: linear-gradient(180deg, #3b0cdc, transparent);
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
