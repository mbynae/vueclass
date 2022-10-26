<template>
  <section id="bannerType" class="banner__wrap" :class="attr">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="title">저녁의 와인 한잔</h3>
      <p class="desc">
        오늘 밤은 좋은 무드를 가지고 와인 한잔 어떨까요?
        <br />
        와인은 포도를 발효시켜 만든 오랜 역사를 가진 양조주입니다.
      </p>
      <span class="small">Let's try to wine!</span>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
};
</script>

<style>
.banner__inner {
  background-image: url(../../assets/img/banner_bg01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: #fff;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1;
  font-weight: 300;
  margin-bottom: 40px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
}
.banner__inner .desc a {
  color: #fff;
  display: block;
}
.banner__inner .desc a:hover {
  text-decoration: underline;
}

.banner__inner .small {
  font-size: 16px;
  text-decoration: underline;
}

@media (max-width: 960px) {
  .banner__inner {
    padding: 100px 0;
  }
}
@media (max-width: 600px) {
  .banner__inner {
    padding: 80px 0;
  }
  .banner__inner .title {
    font-size: 30px;
    margin-bottom: 20px;
  }
  .banner__inner .desc {
    font-size: 16px;
    margin-bottom: 40px;
  }
}
</style>
