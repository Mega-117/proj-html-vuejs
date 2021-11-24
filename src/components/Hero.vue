<template>
  <div class="hero" :class="contentHero.bgHero">
    <div class="hero-overlay"></div>
    <div class="container">
      <div :class="contentHero.align">
        <small>{{ contentHero.subTitle }}</small>
        <h1>
          {{ contentHero.title }}
        </h1>

        <button>
          <strong>{{ contentHero.btnText }}</strong>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
  props: {
    contentHero: Object,
  },
};
</script>

<style lang="scss">
@import "@/styles/hero.scss";
</style>