<template>
  <div class="row">
    <div class="col">
      <div class="box" :class="content.align">
        <div class="section-text" :class="content.alignText">
          <h6 v-if="content.textUp">{{ content.textUp }}</h6>
          <h2>{{ content.title }}</h2>
          <p v-if="content.text">
            {{ content.text }}
          </p>
          <small>{{ content.dataText }}</small>
        </div>
        <button class="btn-2" v-if="content.btnText">
          <strong>{{ content.btnText }}</strong>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    content: Object,
  },
};
</script>

<style lang="scss">
.box {
  margin-bottom: 73px;
  .section-text {
    width: 45%;
    h6 {
      padding-bottom: 30px;
    }
    h2 {
      margin-bottom: 25px;
    }
  }
  button {
    border-radius: 30px;
    padding: 10px 15px;
  }
}
</style>