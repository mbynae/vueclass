<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2>365일 언제나 맛있는 과일 쥬스</h2>
    <p>남녀노소 누구에게나 인기있는 생과일 쥬스를 소개합니다!</p>
    <div class="image__inner" :class="layout">
      <article class="image img1">
        <h3 class="image__title">상큼한 오렌지 쥬스</h3>
        <p class="image__desc">
          톡 쏘는 맛과 시원하고 달달한 오랜지 쥬스입니다.
          <br />
          비타민C의 함유량도 엄청나요.
        </p>
        <a class="image__btn" href="/" title="자세히 보기"> 자세히 보기 </a>
      </article>
      <article class="image img2">
        <h3 class="image__title">달콤한 딸기 쥬스</h3>
        <p class="image__desc">
          달달하고 맛있는 딸기쥬스입니다.
          <br />
          한모금 마시면 잊을수가 없는 맛이죠.
        </p>
        <a class="image__btn yellow" href="/" title="자세히 보기">
          자세히 보기
        </a>
      </article>
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
/* imageType */
.image__inner {
  display: flex;
  justify-content: space-between;
}
.image {
  width: 49%;
  height: 370px;
  color: #fff;
  padding: 200px 30px 30px 30px;
  box-sizing: border-box;
}
.image.img1 {
  background: url(../../assets/img/img_bg01.jpg) no-repeat center / cover;
}
.image.img2 {
  background: url(../../assets/img/img_bg02.jpg) no-repeat center / cover;
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.image__desc {
  font-size: 16px;
  font-weight: 300;
  margin-bottom: 10px;
  line-height: 1.5;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
.image__btn {
  font-size: 16px;
  color: #fff;
  background-color: #b45a30;
  padding: 10px 20px;
  display: inline-block;
}
.image__btn.yellow {
  background-color: #b59140;
}

@media (max-width: 960px) {
}
@media (max-width: 600px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
    padding: 210px 20px 20px 20px;
  }
  .image:first-child {
    margin-bottom: 20px;
  }
  .image__title {
    font-size: 24px;
  }
}
</style>
