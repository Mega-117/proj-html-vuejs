<template>
  <main>
    <Hero></Hero>
    <div class="promo">
      <div class="container">
        <div class="d-flex justify-content-center align-items-center">
          <img src="../assets/food-transparent-5-200x112.png" alt="" />
          <span>
            Get $25 OFF your first purchase of our homemade pet food!</span
          >
          <a href="#">Visit the shop</a>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Hero from "@/components/Hero.vue";
export default {
  name: "Main",
  components: {
    Hero,
  },
};
</script>

<style scoped lang="scss">
@import "@/styles/main.scss";
</style>