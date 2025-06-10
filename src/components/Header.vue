<template>
  <div class="w-100">
    <div class="container">
      <nav class="navbar navbar-expand-lg">
        <router-link class="navbar-brand logo" to="/">
          <img :src="logoUrl" alt="Logo" />
        </router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-0 gap-3">
            <li class="nav-item" v-for="(item, index) in navItems" :key="index">
              <router-link class="nav-link" :to="item.link">
                <img src="@/assets/icon/menu-icon.svg" />
                {{ item.label }}
              </router-link>
            </li>
            <li class="nav-item bc-1 br-1 logIn">
              <router-link class="nav-link">
                <img src="@/assets/icon/menu-icon.svg" />
                登入
              </router-link>
            </li>
          </ul>
        </div>
      </nav>
    </div>
  </div>
</template>

<script setup>
import logoUrl from "@/assets/images/logo.png";
const navItems = [
  { label: "首頁", link: "/" },
  { label: "合作刊登", link: "/" },
  { label: "專案一覽", link: "/" },
  { label: "啟動/參與", link: "/" },
  { label: "創媒之星", link: "/" },
  { label: "門市分布", link: "/" },
];
</script>
<style lang="scss" scoped>
.w-100 {
  z-index: 99;
  position: relative;
}

.container {
  padding-top: 1.5rem;
}

.navbar {
  background: linear-gradient(to bottom, #ff714acc, #ff5f31cc);
  box-shadow: 0px 4px 6px rgba(87, 80, 78, 0.25);
  backdrop-filter: blur(3px);
  padding: 10px 40px;
  border-radius: 50px;
  height: 70px;

  @media (max-width: 767px) {
    padding: 10px 25px;
    position: relative;
  }
  &-nav {
    @media (max-width: 767px) {
      border-radius: 12px;
      padding: 10px;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      background: linear-gradient(
        to bottom,
        rgba(255, 113, 74, 1),
        rgba(255, 95, 49, 1)
      );
    }
    li {
      .nav-link {
        font-weight: 600;
        font-size: 16px;
        color: #fff;
        line-height: 19px;
        letter-spacing: 2px;
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        @media (max-width: 767px) {
          padding: 10px 0;
          width: 100%;
        }
      }
    }
  }

  &-collapse {
    @media (max-width: 767px) {
      position: absolute;
      top: 100%;
      left: 0;
      width: 100%;
      background: linear-gradient(to bottom, #ff714a, #ff5f31);
      padding: 1rem;
      z-index: 98;
      border-radius: 12px;
    }
  }
}
</style>
