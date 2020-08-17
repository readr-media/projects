<section class="desktop-wrapper">
  <Header />
  <section class="landing-wrapper">
    <div class="landing-wrapper__info-wrapper info-wrapper">
      <div class="info-wrapper__description">
        <p>潘小俠是一個攝影家，拍照至今 40 年，曾獲頒 40 屆吳三連藝術獎，作品被北美館、台灣美術館典藏。他出身攝影記者，當過歌手經紀人，開過 PUB，無論身份為何，鏡頭始終對準台灣島上的人與事。從蘭嶼達悟族人到艋舺茶室小姐和遊民，從美術家、作家到白色恐怖受難者，他的每項主題拍攝時間動輒一、二十年，靠著長久而近距離的注視，為每一張曾在島嶼上生活的臉孔作記。</p>
      </div>
      <img
        class="info-wrapper__landing-image"
        src="img/figure-1954-1.jpg"
        alt="landing-image"
      >
      <h1 class="info-wrapper__title">
        <img src="img/title-w.svg" alt="title">
      </h1>
    </div>
  </section>
  <Youtube />
  <Footer />
</section>

<script>
  import Header from '../components/Header.svelte'
  import Footer from '../components/Footer.svelte'
  import Youtube from '../components/Youtube.svelte'
</script>

<style lang="scss">
  .landing-wrapper {
    display: flex;
    align-items: center;
    min-height: 100vh;
    position: relative;
  }
  .info-wrapper {
    width: 100%;
    padding-top: 34%;
    height: 0;
    position: relative;
    top: 80px;
    &__title {
      position: absolute;
      top: -12vw;
      left: 0;
      width: 80%;
      margin: 0 0 0 20px;
      img {
        width: 100%;
        height: 100%;
      }
    }
    &__description {
      position: absolute;
      top: 0;
      left: 0;
      width: 50%;
      height: 100%;
      padding: 84px 110px;
      background-color: #d8d8d8;
      font-size: 16px;
      line-height: 1.88;
      text-align: justify;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &__landing-image {
      position: absolute;
      top: 0;
      left: 50%;
      width: 50%;
      height: 100%;
    }
  }
  
  @media (max-width: 1200px) {
    .info-wrapper {
      &__description {
        padding: 84px 20px;
      }
    }
  }
</style>