<template>
  <div class="service-icon-wrapper d-flex justify-content-center gap-4 mt-5">
    <div class="service-icon" v-for="(item, index) in icons" :key="index">
      <img :src="item.img" height="150" class="mb-3" />
      <h3>{{ item.title }}</h3>
      <hr />
      <span>{{ item.description }}</span>
    </div>
  </div>
</template>

<script setup>
defineProps({
  icons: {
    type: Array,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.service {
  &-icon {
    h3 {
      font-family: "Noto Sans TC";
      font-style: normal;
      font-weight: 700;
      font-size: 24px;
      line-height: 29px;
      letter-spacing: 2px;
      text-align: center;
      color: #ff6634;
    }
    hr {
      border: 2px solid #f64c24;
    }
    span {
      // font-family: "Noto Sans TC";
      // font-style: normal;
      font-weight: 400;
      font-size: 18px;
      line-height: 26px;
      color: #373a36;
    }
  }
}
</style>
