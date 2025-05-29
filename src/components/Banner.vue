<template>
  <div class="banner">
    <div class="banner-content">
      <img src="@/assets/images/banner.jpg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner",
};
</script>
<style lang="scss" scoped>
.banner {
  margin-top: -94px;
  &-content {
    img {
      width: 100%;
    }
  }
}
</style>
