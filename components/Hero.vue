<template>
  <div class="hero">
    <p class="hero-eyebrow">Yar Pirate Ipsum</p>
    <h1 class="hero-title">
      Hail-shot ahoy furl bilge yard topsail Jolly Roger overhaul Spanish Main.
    </h1>
    <h2 class="hero-subtitle">
      Jack Ketch trysail code of conduct quarterdeck barque lugger reef sails
      Blimey bowsprit run a rig warp parrel.
    </h2>
  </div>
</template>

<style scoped>
/* clamp(MIN, VAL, MAX) is resolved as max(MIN, min(VAL, MAX)) */
.hero {
  max-width: 600px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.hero-eyebrow {
  text-transform: uppercase;
  color: white;
  font-size: 1rem;
  font-weight: bold;
  letter-spacing: -1px;
  margin-bottom: 0.3125rem;
}
.hero-title {
  color: white;
  font-size: clamp(1.5rem, 5vw, 2rem);
  font-weight: normal;
  padding-right: 3rem;
  padding-left: 3rem;
  margin-bottom: 1rem;
}
.hero-subtitle {
  color: white;
  font-size: max(0.75rem, 1vw);
  font-weight: normal;
  padding-right: 1rem;
  padding-left: 1rem;
}
@media only screen and (min-width: 768px) {
  .hero {
    flex-grow: 1;
  }
}
</style>
