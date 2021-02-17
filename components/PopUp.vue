<template>
  <div class="popup-container">
    <div class="popup-title">
      <h1>{{ title }}</h1>
      <h2>{{ subTitle }}</h2>
    </div>
    <iframe
      allowfullscreen
      class="video-iframe"
      frameborder="0"
      :src="`${iframeSrc}`"
    ></iframe>
    <div class="popup-menu">
      <button type="button" class="close" @click="closePopup">
        Back to Home
      </button>
      <p>Prow scuttle parrel</p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'PopUp',
  props: {
    title: {
      type: String,
      required: true,
    },
    subTitle: {
      type: String,
      required: true,
    },
    closePopup: {
      type: Function,
      required: true,
      default: () => false,
    },
    iframeSrc: {
      type: String,
      required: true,
    },
  },
})
</script>

<style scoped>
.popup-container {
  width: 100%;
  height: 100vh;
  position: relative;
  overflow: hidden;
}

.video-iframe {
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  border: 0;
  background: #3c3c3b;
}

.popup-title {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  z-index: 5;
}

.popup-menu {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 5;
  display: flex;
  justify-content: space-between;
}
</style>
