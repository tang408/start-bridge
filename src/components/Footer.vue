<template>
  <div class="footer">
    <div class="container">
      <div class="col-6">
        <div class="col-2">
          <img src="@/assets/images/logo-white.png" class="w-100" alt="" />
        </div>
        <div class="col-5">
          <div class="information">
            <span>台北市信義區松德路OOOOO </span>
            <span>OOOOOOOO@gmail.com</span>
            <span>02-23456789</span>
          </div>
        </div>
        <div class="col-5 statement">
          <span>平台合約聲明</span><span>版權內容</span>
        </div>
      </div>
      <div class="col-6 community">
        <img src="@/assets/images/line.png" />
        <img src="@/assets/images/ig.png" />
        <img src="@/assets/images/fb.png" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
.footer {
  background: linear-gradient(180deg, #ff9966 0%, #ff6634 100%);
  color: #fff;
  height: 311px;
  align-content: center;
  .container {
    display: flex;
    @media (max-width: 767px) {
      display: block;
    }
    .col-6 {
      display: flex;
      &.community {
        gap: 10px;
        justify-content: end;
        align-items: center;
        img {
          width: 30px;
          height: 30px;
        }
      }
    }
    .col-5 {
      align-content: center;
      justify-content: center;
      display: grid;
      .information {
        display: inline-flex;
        flex-flow: column;
      }
      &.statement {
        display: flex;
        align-items: center;
        gap: 10px;
      }
    }
  }
}
</style>
