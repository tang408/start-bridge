<template>
  <div class="service">
    <div class="container pb-05">
      <div class="d-flex justify-content-center service-btn">
        <button class="service-btn-yellow">
          <img src="@/assets/icon/btn-icon.svg" />【啟動】創業
        </button>
        <button class="service-btn-black">
          <img src="@/assets/icon/btn-icon2.svg" />【參與】共創
        </button>
      </div>
      <div class="service-title">
        <h1>全方位創業媒合服務</h1>
        <span>星橋為您繫起，步步實踐成功的橋樑</span>
      </div>
      <div class="service-card">
        <img src="@/assets/images/service-card.png" class="w-100" />
      </div>
      <div>
        <ServiceIcon :icons="serviceIcons" />
      </div>
    </div>
    <div class="service-progress">
      <img src="@/assets/images/shape1.svg" class="service-progress-shape1" />
      <img src="@/assets/images/shape2.svg" class="service-progress-shape2" />
      <div class="container">
        <SharedSwiper
          :cards="progressCards"
          prevElClass="progress-prev-1"
          nextElClass="progress-next-1"
        />
      </div>
    </div>
    <div class="service-project">
      <div class="container">
        <SharedSwiper
          :cards="progressCards"
          prevElClass="progress-prev-2"
          nextElClass="progress-next-2"
        />
        <button class="service-project-btn mt-5" @click="goMoreProjects">
          更多專案
        </button>
      </div>
    </div>

    <div class="service-process">
      <div class="container">
        <div class="service-title">
          <h1>服務流程</h1>
          <span>星橋撐腰，雙向安心，輕鬆啟程</span>
        </div>
        <div class="process-flow">
          <div class="process-cards">
            <div
              class="process-card"
              v-for="(step, index) in processCardSteps"
              :key="index"
            >
              <img :src="step.img" class="process-image" />
              <div class="btn-tooltip-wrapper">
                <div class="process-btn">{{ step.title }}</div>
                <div class="process-tooltip">{{ step.desc }}</div>
              </div>
            </div>
          </div>

          <div class="process-step">
            <div class="process-step-tracker">
              <div
                class="step"
                v-for="(step, index) in processSteps"
                :key="'step-' + index"
                :class="{ active: index === 0 }"
              >
                {{ index + 1 }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import ServiceIcon from "../components/Service-Icon.vue";
import SharedSwiper from "./SharedSwiper.vue";

const serviceIcons = [
  {
    img: new URL("@/assets/images/service-icon1.svg", import.meta.url).href,
    title: "創業不迷航",
    description: "從評估到加盟，專員陪跑解決焦慮。",
  },
  {
    img: new URL("@/assets/images/service-icon2.svg", import.meta.url).href,
    title: "嚴選連鎖品牌",
    description: "嚴選優質成熟品牌，複製成功模式。",
  },
  {
    img: new URL("@/assets/images/service-icon3.svg", import.meta.url).href,
    title: "雲端資料庫",
    description: "即時瀏覽品牌資訊、串接全台人脈網絡。",
  },
  {
    img: new URL("@/assets/images/service-icon4.svg", import.meta.url).href,
    title: "低門檻參與",
    description: "告別盲目投入，小額滾出大收益。",
  },
  {
    img: new URL("@/assets/images/service-icon5.svg", import.meta.url).href,
    title: "實戰進修輔導",
    description: "輔導課程、專業講座、業師培訓一應俱全。",
  },
];

const progressCards = [
  {
    id: 1,
    img: new URL("@/assets/images/card-box.png", import.meta.url).href,
    // tags: ["預購商品", "支援配送"],
    title: "專案名稱專案名稱區域專案名稱專案名稱區域專案名稱",
    progress: 88,
    price: "99天",
    supporters: "9999 人瀏覽",
  },
  {
    id: 2,
    img: new URL("@/assets/images/card-box.png", import.meta.url).href,
    // tags: ["預購商品", "支援配送"],
    title: "專案名稱專案名稱區域專案名稱專案名稱區域專案名稱",
    progress: 72,
    price: "99天",
    supporters: "9999 人瀏覽",
  },
  {
    id: 3,
    img: new URL("@/assets/images/card-box.png", import.meta.url).href,
    // tags: ["預購商品", "支援配送"],
    title: "專案名稱專案名稱區域專案名稱專案名稱區域專案名稱",
    progress: 55,
    price: "99天",
    supporters: "9999 人瀏覽",
  },
  {
    id: 4,
    img: new URL("@/assets/images/card-box.png", import.meta.url).href,
    // tags: ["預購商品", "支援配送"],
    title: "專案名稱專案名稱區域專案名稱專案名稱區域專案名稱",
    progress: 91,
    price: "99天",
    supporters: "9999 人瀏覽",
  },
  {
    id: 5,
    img: new URL("@/assets/images/card-box.png", import.meta.url).href,
    // tags: ["預購商品", "支援配送"],
    title: "專案名稱專案名稱區域專案名稱專案名稱區域專案名稱",
    progress: 64,
    price: "99天",
    supporters: "9999 人瀏覽",
  },
];

const processCardSteps = [
  {
    img: new URL("@/assets/images/process-step1.png", import.meta.url).href,
    title: "線上註冊",
    desc: "對接創業者與品牌需求，提交申請，啟動媒合。",
  },
  {
    img: new URL("@/assets/images/process-step2.png", import.meta.url).href,
    title: "門店諮詢",
    desc: "預約到訪諮詢據點，專業團隊解析最優方案。",
  },
  {
    img: new URL("@/assets/images/process-step3.png", import.meta.url).href,
    title: "專員對接",
    desc: "化身陪跑夥伴協作支持，主動促進合作方溝通協調。",
  },
  {
    img: new URL("@/assets/images/process-step4.png", import.meta.url).href,
    title: "合作支持",
    desc: "簽訂媒合協議，保障權益，提供持續資源與轉型服務。",
  },
];

const processSteps = [1, 2, 3, 4];
</script>

<style lang="scss" scoped>
.service {
  background-image: url("@/assets/images/service.png");
  background-repeat: no-repeat;
  padding: 2rem 0;
  text-align: center;

  &-btn {
    gap: 1rem;
    margin-bottom: 3rem;
    button {
      font-weight: 500;
      font-size: 22px;
      line-height: 26px;
      display: flex;
      align-items: center;
      letter-spacing: 2px;
      box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
      padding: 10px 20px;
      gap: 8px;
      border-radius: 50px;
      border: none;
      width: 400px;
      justify-content: center;
    }
    &-yellow {
      color: #000000;
      background-color: #ffc919;
    }

    &-black {
      color: #ffffff;
      background-color: #262626;
    }

    img {
      width: 17px;
      height: 24px;
    }
  }

  &-title {
    // margin-top: 3rem;
    letter-spacing: 0.1em;
    h1 {
      font-weight: 700;
      font-size: 36px;
      line-height: 43px;
      letter-spacing: 0.1em;
    }
    span {
      font-weight: 400;
      font-size: 16px;
      line-height: 19px;
    }
  }

  &-card {
    margin-top: 3rem;
  }

  &-progress {
    background-color: #ffcc66;
    position: relative;
    &-shape1 {
      position: absolute;
      left: 0;
      top: -170px;
    }
    &-shape2 {
      position: absolute;
      right: 0;
      bottom: -20%;
    }
  }
}

.service-progress {
  padding: 4rem 0;
}

.service-project {
  padding: 4rem 0;
  background-image: url("@/assets/images/service-project.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  &-btn {
    padding: 10px 24px;
    font-size: 16px;
    color: #fff;
    cursor: pointer;
    font-weight: bold;
    background: linear-gradient(0deg, #262626, #262626),
      linear-gradient(126.86deg, #665f51 -8.87%, #b86a54 112.15%);
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
    border-radius: 50px;
    border: none;

    width: 35%;
    &:hover {
      background: #000000;
    }
  }
}

.service-process {
  padding: 4rem 0;
  background: linear-gradient(
    90deg,
    rgba(236, 236, 236, 0.5) 0%,
    rgba(213, 213, 213, 1) 100%
  );

  .process-cards {
    display: flex;
    justify-content: space-between;
    gap: 2rem;
    margin-top: 3rem;

    .process-card {
      width: 22%;
      text-align: center;
      position: relative;
      display: flex;
      flex-flow: column;
      align-items: center;

      .process-image {
        width: 320px;
        height: 320px;
      }

      .btn-tooltip-wrapper {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
      }

      .process-btn {
        background-color: #333;
        color: #fff;
        padding: 10px 20px;
        border-radius: 50px;
        font-weight: bold;
        cursor: pointer;
        display: inline-block;
        width: 200px;
        font-size: 24px;
        z-index: 1;
      }

      .process-tooltip {
        margin-top: -1rem;
        padding: 25px 20px;
        width: 250px;
        border-radius: 8px;
        position: relative;
        opacity: 0;
        visibility: hidden;
        transition: opacity 0.3s ease;
        min-height: 60px;
        border: 2px solid;
        font-weight: 500;
        font-size: 16px;
        line-height: 19px;
        text-align: center;
        letter-spacing: 0.1em;
        color: #000000;
      }

      .btn-tooltip-wrapper:hover .process-tooltip {
        opacity: 1;
        visibility: visible;

        &::after {
          opacity: 1;
        }
      }
    }
  }
  .process-step {
    width: 100%;
    display: flex;
    justify-content: center;
    &-tracker {
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: relative;
      margin-top: 2rem;
      padding: 0;
      width: 1050px;

      &::before {
        content: "";
        position: absolute;
        top: 50%;
        left: 0;
        right: 0;
        height: 2px;
        background-color: #ccc;
        transform: translateY(-50%);
        z-index: 0;
      }

      .step {
        position: relative;
        z-index: 1;
        width: 26px;
        height: 26px;
        border-radius: 50%;
        border: 2px solid #999;
        background-color: #fff;
        color: #333;
        display: flex;
        justify-content: center;
        align-items: center;
        font-weight: bold;
        font-size: 14px;
        background: #fff;
      }

      .step.active {
        background-color: #333;
        color: #fff;
        border-color: #333;
      }
    }
  }
}
</style>
