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
  top: 15%;
  left: 0;
  right: 0;
  z-index: 5;
  padding-right: 5vw;
  padding-left: 5vw;
}

.popup-title h1 {
  font-style: normal;
  font-weight: bold;
  font-size: clamp(0.875rem, 5vw, 1.75rem);
  line-height: clamp(0.9375rem, 5vw, 1.9375rem);
  text-align: center;
  color: #fff;
}

.popup-title h2 {
  font-style: normal;
  font-weight: 500;
  font-size: clamp(0.875rem, 5vw, 1.25rem);
  line-height: clamp(0.9375rem, 5vw, 1.375rem);
  text-align: center;
  text-transform: uppercase;
  color: #fff;
  margin-top: 6px;
}

.popup-menu {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 5;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 72px;
  background: rgba(35, 31, 32, 0.65);
  padding-right: 3.5vw;
  padding-left: 3.5vw;
}

.close {
  font-style: normal;
  font-weight: 500;
  font-size: 0.75rem;
  line-height: 0.75rem;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: #fff;
}

.popup-menu p {
  font-style: normal;
  font-weight: 500;
  font-size: 0.75rem;
  line-height: 0.75rem;
  text-align: right;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: #fff;
}
</style>
