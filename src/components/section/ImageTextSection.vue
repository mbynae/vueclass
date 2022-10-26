<template>
  <section id="imgTextType" class="mgText__wrap" :class="attr">
    <h2 class="blind">계절별 제철 과일 알아보기</h2>
    <div class="imgText__inner" :class="layout">
      <div class="imgText__txt">
        <span>Seasonal Fruits</span>
        <h3>계절별 제철 과일 알아보기</h3>
        <p>
          과일은 봄여름가을겨울 그리고 지역에 따라 제배 종류가 달라지죠. 다양한
          과일을 알아봅시다.
        </p>
        <ul>
          <li>
            <a href="/">봄 제철 과일</a>
          </li>
          <li>
            <a href="/">여름 제철 과일</a>
          </li>
          <li>
            <a href="/">가을 제철 과일</a>
          </li>
          <li>
            <a href="/">겨울 제철 과일</a>
          </li>
          <li>
            <a href="/">열대 지역 과일</a>
          </li>
          <li>
            <a href="/">한랭 지역 과일</a>
          </li>
        </ul>
      </div>
      <div class="imgText__img img1">
        <a href="/">열대 과일</a>
      </div>
      <div class="imgText__img img2">
        <a href="/" class="blue"> 한랭 과일 </a>
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
/* imgTextType */
.imgText__inner {
  display: flex;
  justify-content: space-between;
}
.imgText__inner > div {
  width: 32%;
  height: 500px;
}
.imgText__txt span {
  font-size: 16px;
  color: #666;
  text-decoration: underline;
  text-underline-position: under;
  margin-bottom: 20px;
  display: block;
}
.imgText__txt h3 {
  font-size: 50px;
  font-weight: 300;
  word-break: keep-all;
  margin-bottom: 20px;
}
.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  margin-bottom: 10px;
  color: #666;
}
.imgText__txt ul {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.6;
}
.imgText__txt ul li {
  position: relative;
  padding-left: 20px;
}
.imgText__txt ul li a {
  color: #666;
}
.imgText__txt ul li::before {
  content: "";
  width: 5px;
  height: 5px;
  border-radius: 50%;
  position: absolute;
  left: 5px;
  top: 9px;
  background: #666;
}
.imgText__img {
  border-radius: 10px;
  position: relative;
}
.imgText__img a {
  position: absolute;
  left: 30px;
  bottom: 30px;
  background-color: #7c2b39;
  color: #fff;
  padding: 10px 30px;
  font-size: 18px;
  border-radius: 30px;
  display: inline-block;
}
.imgText__img a.blue {
  background-color: #2b387c;
}
.imgText__img.img1 {
  background: url(../../assets/img/imgText_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/imgText_bg02.jpg) no-repeat center / cover;
}

@media (max-width: 960px) {
  .imgText__inner {
    flex-wrap: wrap;
  }
  .imgText__txt h3 {
    font-size: 40px;
    margin-bottom: 20px;
  }
  .imgText__txt p {
    margin-bottom: 60px;
  }
  .imgText__inner > div.imgText__txt {
    width: 100%;
    height: auto; /*height값 초기화*/
    text-align: center;
  }
  .imgText__inner > div.imgText__txt ul {
    display: none;
  }
  .imgText__inner > div.imgText__img {
    width: 49%;
  }
}
@media (max-width: 600px) {
  .imgText__txt span {
    font-size: 14px;
    margin-bottom: 10px;
  }
  .imgText__txt h3 {
    font-size: 30px;
  }
  .imgText__txt p {
    margin-bottom: 50px;
    font-size: 16px;
  }
  .imgText__inner > div.imgText__img {
    width: 100%;
    height: 200px;
  }
  .imgText__inner > div.imgText__img.img1 {
    margin-bottom: 20px;
  }
  .imgText__img a {
    left: 20px;
    bottom: 20px;
  }
}
</style>
