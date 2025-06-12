<template>
  <div class="footer">
    <div class="container">
      <div class="col-sm-6 col-12">
        <div class="col-sm-2 col-12">
          <img src="@/assets/images/logo-white.png" class="footer-logo" />
        </div>

        <div class="col-sm-6 col-12 community desktop-flex-none">
          <img src="@/assets/images/line.png" />
          <img src="@/assets/images/ig.png" />
          <img src="@/assets/images/fb.png" />
        </div>
        <div class="col-sm-5 col-12">
          <div class="information">
            <span>台北市信義區松德路OOOOO </span>
            <span>OOOOOOOO@gmail.com</span>
            <span>02-23456789</span>
          </div>
        </div>
        <div class="col-sm-5 col-12 statement">
          <span>平台合約聲明</span><span>版權內容</span>
        </div>
      </div>
      <div class="col-sm-6 col-12 community mobile-none">
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
  @media (max-width: 767px) {
    height: 596px;
  }
  .container {
    display: flex;
    @media (max-width: 767px) {
      flex-flow: column;
      align-items: center;
      text-align: center;
      gap: 30px;
    }
    .col-sm-6 {
      display: flex;
      @media (max-width: 767px) {
        display: contents;
      }

      &.community {
        gap: 10px;
        justify-content: end;
        align-items: center;
        @media (max-width: 767px) {
          display: flex;
          justify-content: center;
        }
        img {
          width: 30px;
          height: 30px;
        }
      }
    }
    .col-sm-5 {
      align-content: center;
      justify-content: center;
      display: grid;
      .information {
        display: inline-flex;
        flex-flow: column;
        @media (max-width: 767px) {
          display: flex;
          flex-flow: column;
          gap: 5px;
        }
      }
      &.statement {
        display: flex;
        align-items: center;
        gap: 10px;
        @media (max-width: 767px) {
          flex-flow: column;
          gap: 0;
        }
      }
    }
  }
  &-logo {
    width: 100%;
    @media (max-width: 767px) {
      width: 145px;
    }
  }
}
</style>
