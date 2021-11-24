<template>
  <div class="bg-dog" :class="content[0].align">
    <div class="container">
      <div v-if="content[0].testimonials" class="text-white text-center">
        <h1>Users testimonials</h1>
      </div>
      <div class="row">
        <div v-for="(el, i) in content" :key="i" class="col">
          <div class="text-white text-center">
            <div class="img-container d-flex justify-content-center">
              <div v-if="el.src" class="overlay">
                <img :src="el.src" alt="" />
              </div>
              <i :class="el.icon" aria-hidden="true"></i>
            </div>
            <p v-if="el.text">
              {{ el.text }}
            </p>
            <small>{{ el.name }}</small>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GreenBlock",
  props: {
    content: Array,
  },
};
</script>

<style lang="scss">
@import "@/styles/greenBlock.scss";
</style>