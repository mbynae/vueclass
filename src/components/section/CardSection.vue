<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>과일로 만든 다양한 음식</h2>
    <p>과일로 만든 맛있고 다양한 대표적인 음식을 소개합니다!</p>
    <div class="card__inner" :class="layout">
      <article class="card">
        <figure class="card__header">
          <img
            src="assets/img/card_bg01_01.jpg"
            alt="아기 리트리버에 대해 알아보기"
          />
        </figure>
        <div class="card__body">
          <h3 class="title">과일 샐러드</h3>
          <p class="desc">
            과일 샐러드는 다양한 야채와 과일을 섞어 넣고 소스에 버무려 먹는
            대표적인 과일 음식입니다. 다양한 음식과 어울리며, 콘프레이크,
            드레싱, 요구르트 등과 곁들어 먹기도 합니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="71"
                height="8"
                viewBox="0 0 71 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M70.3536 4.35355C70.5488 4.15829 70.5488 3.84171 70.3536 3.64645L67.1716 0.464466C66.9763 0.269204 66.6597 0.269204 66.4645 0.464466C66.2692 0.659728 66.2692 0.976311 66.4645 1.17157L69.2929 4L66.4645 6.82843C66.2692 7.02369 66.2692 7.34027 66.4645 7.53553C66.6597 7.7308 66.9763 7.7308 67.1716 7.53553L70.3536 4.35355ZM0 4.5H70V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img
            src="assets/img/card_bg01_02.jpg"
            alt="아기 리트리버에 대해 알아보기"
          />
        </figure>
        <div class="card__body">
          <h3 class="title">과일 타르트</h3>
          <p class="desc">
            과일 타르트는 비스켓 위에 크림과 갖가지 과일을 올려 먹는 달콤한
            과자입니다. 유럽에서 오랜 역사를 가지고 있으며, 나라와 지역별로
            종류도 다양해 많은 나라에서 사랑받고 있습니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="71"
                height="8"
                viewBox="0 0 71 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M70.3536 4.35355C70.5488 4.15829 70.5488 3.84171 70.3536 3.64645L67.1716 0.464466C66.9763 0.269204 66.6597 0.269204 66.4645 0.464466C66.2692 0.659728 66.2692 0.976311 66.4645 1.17157L69.2929 4L66.4645 6.82843C66.2692 7.02369 66.2692 7.34027 66.4645 7.53553C66.6597 7.7308 66.9763 7.7308 67.1716 7.53553L70.3536 4.35355ZM0 4.5H70V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
      </article>
      <article class="card">
        <figure class="card__header">
          <img
            src="assets/img/card_bg01_03.jpg"
            alt="아기 리트리버에 대해 알아보기"
          />
        </figure>
        <div class="card__body">
          <h3 class="title">과일 화채</h3>
          <p class="desc">
            과일 화채는 탄산수나 우유에 과일을 넣어 시원하게 해서 먹는 여름용
            별미 음식입니다. 화채는 우리나라의 전통 음식으로 다양한 화채가
            존재하나 특히 과일 화채가 가장 사랑받고 있습니다.
          </p>
          <a class="btn" href="/">
            더 자세히 보기
            <span aria-hidden="true">
              <svg
                width="71"
                height="8"
                viewBox="0 0 71 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M70.3536 4.35355C70.5488 4.15829 70.5488 3.84171 70.3536 3.64645L67.1716 0.464466C66.9763 0.269204 66.6597 0.269204 66.4645 0.464466C66.2692 0.659728 66.2692 0.976311 66.4645 1.17157L69.2929 4L66.4645 6.82843C66.2692 7.02369 66.2692 7.34027 66.4645 7.53553C66.6597 7.7308 66.9763 7.7308 67.1716 7.53553L70.3536 4.35355ZM0 4.5H70V3.5H0V4.5Z"
                  fill="black"
                />
              </svg>
            </span>
          </a>
        </div>
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
.card__inner {
  display: flex;
  justify-content: space-around;
}
.card {
  width: 32%;
  background: #f5f5f5;
}
.card__body {
  padding: 24px;
}
.card__body .title {
  font-size: 24px;
  margin-bottom: 10px;
  overflow: hidden; /* 여기부터 아래까지 1줄 효과 */
  white-space: nowrap;
  text-overflow: ellipsis;
  padding-right: 20px;
}
.card__body .desc {
  font-size: 18px;
  line-height: 1.4;
  color: #666;
  margin-bottom: 20px;
  font-weight: 300;
  overflow: hidden; /* 여기부터 아래까지 3줄 효과 */
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
}
.card__body .btn {
}

@media (max-width: 960px) {
  .card__inner {
    flex-wrap: wrap;
  }
  .card {
    width: 49%;
  }
  .card:last-child {
    display: none;
  }
}
@media (max-width: 600px) {
  .card {
    width: 100%;
  }
  .card:first-child {
    margin-bottom: 20px;
  }
  .card__body {
    padding: 20px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}
</style>
