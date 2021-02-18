<template>
  <div>
    <div class="container">
      <div class="content">
        <PopUp
          v-if="showBtnOne"
          title="Deadlights jack lad"
          sub-title="callywag dance the hempen jig carouser"
          iframe-src="https://player.vimeo.com/video/310438775?title=0&amp;portrait=0&amp;byline=0&amp;autoplay=1"
          :close-popup="closePopup"
        />
        <PopUp
          v-if="showBtnTwo"
          title="Deadlights jack lad 2"
          sub-title="spyglass sheet transom heave to"
          iframe-src="https://player.vimeo.com/video/216445847?title=0&portrait=0&byline=0&autoplay=1"
          :close-popup="closePopup"
        />
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
      this.showBtnOne = !this.showBtnOne
    },
    toggleBtnTwo() {
      this.showBtnTwo = !this.showBtnTwo
    },
    closePopup() {
      if (this.showBtnOne) {
        this.showBtnOne = !this.showBtnOne
      }

      if (this.showBtnTwo) {
        this.showBtnTwo = !this.showBtnTwo
      }
    },
  },
})
</script>

<style>
button {
  border: 0;
  margin: 0;
  padding: 0;
  border-radius: 0;
  background: transparent;
  appearance: none;
  text-decoration: none;
  cursor: pointer;
}

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
  background: linear-gradient(180deg, #dc780c, transparent);
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
