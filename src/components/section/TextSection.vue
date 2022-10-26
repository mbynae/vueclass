<template>
  <section id="textType" class="text__wrap" :class="attr">
    <span>Colors of fruits</span>
    <h2 class="mb70">6가지 색깔의 과일</h2>
    <div class="text__inner" :class="layout">
      <div class="text t1">
        <h3 class="text__title">빨간색(Red)</h3>
        <p class="text__desc">
          화려하고 정렬적인 빨간색은 사람의 식욕을 돋구는 특징이 있습니다. 이런
          식욕을 돋구는 색을 가진 과일은 딸기, 체리, 사과 등 다양하죠.
        </p>
        <a class="text_btn" href="/"> 더보기 </a>
      </div>
      <div class="text t2">
        <h3 class="text__title">노란색(Yellow)</h3>
        <p class="text__desc">
          명량하고 달콤한 느낌을 주는 노란색의 음식은 바나나가 대표하고
          있습니다. 또한 열대과일 하면 빼놓을 수 없는 파인애플도 있죠!
        </p>
        <a class="text_btn" href="/"> 더보기 </a>
      </div>
      <div class="text t3">
        <h3 class="text__title">초록색(Green)</h3>
        <p class="text__desc">
          마음이 진정되는 자연의 색인 초록색 역시 맛있는 과일을 내포하고
          있습니다. 달콤한 멜론부터 시큼한 매실까지 맛도 다양하죠.
        </p>
        <a class="text_btn" href="/"> 더보기 </a>
      </div>
      <div class="text t4">
        <h3 class="text__title">오랜지색(Orange)</h3>
        <p class="text__desc">
          오랜지색은 말 그대로 오랜지의 색깔입니다. 세계 많은 나라에서 사랑받는
          오랜지는 한라봉, 천혜향 등 종류도 다양하며, 가볍게 먹는 귤 역시
          대표적인 과일입니다.
        </p>
        <a class="text_btn" href="/"> 더보기 </a>
      </div>
      <div class="text t5">
        <h3 class="text__title">보라색(Purple)</h3>
        <p class="text__desc">
          대표적인 보라색 과일하면 역시 포도죠! 과일로도, 와인으로도 너무나도
          다양하게 쓰이는 음식입니다. 또한 여러 베리류 과일 역시 사랑받는
          과일입니다.
        </p>
        <a class="text_btn" href="/"> 더보기 </a>
      </div>
      <div class="text t6">
        <h3 class="text__title">분홍색(Pink)</h3>
        <p class="text__desc">
          빨간색보다 은은하고 부드러운 느낌을 주는 분홍색도 달달하고 향기로운
          식욕을 주는 색입니다. 분홍색에 속하는 과일로는 복숭아와 연한 색깔의
          수박 등 보기만 해도 침이 고이는 음식이 있죠.
        </p>
        <a class="text_btn" href="/"> 더보기 </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
};
</script>

<style>
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}
.text:hover {
  background: #f5f5f5;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  white-space: nowrap;
  text-overflow: ellipsis;
  position: relative;
  padding-top: 75px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  background: url(../../assets/img/text_icon.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  color: #666;
  margin-bottom: 20px;
}
.text_btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  text-underline-position: under;
  color: #666;
}

@media (max-width: 960px) {
  .text {
    width: 49%;
    background: #f5f5f5;
  }
}
@media (max-width: 600px) {
  .text__title {
    font-size: 20px;
  }
  .text__desc {
    font-size: 16px;
  }
}
@media (max-width: 480px) {
  .text {
    width: 100%;
  }
}
</style>
