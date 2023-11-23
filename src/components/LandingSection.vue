<template>
  <div class="landing-section">
    <img
      :src="logo"
      alt=""
      class="landing-section__logo"
    >
    <div class="landing-section__title">
      Sebentar Lagi, Anak Anda Akan Jadi Pusat Perhatian Saat Bicara di Depan Banyak Orang
    </div>
    <div class="landing-section__description">
      Kami mengajarkan anak Anda bagaimana memikat audience dengan teknik yang ga diajarkan di tempat lain
    </div>
    <a href="https://aktlivingacademy.com">
      <button class="landing-section__button">
        Daftar Sekarang
      </button>
    </a>
  </div>
</template>

<script>
import logo from '@/assets/logo.svg'
export default {
  name: 'LandingSection',

  data () {
    return {
      logo
    }
  }
}
</script>

<style scoped>
.landing-section {
  background-image: linear-gradient(#614d1c, #614d1c), url('../assets/landing-img.png');
  min-height: calc(100vh - 76px);
  background-size: cover;
  background-blend-mode: soft-light;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.landing-section__logo {
  filter: brightness(0) invert(1);
  margin-bottom: 20px;
}
.landing-section__title {
  color: white;
  font-size: 24px;
  font-weight: 800;
  margin-bottom: 10px;
  text-align: center;
}

.landing-section__description {
  color: white;
  font-size: 14px;
  font-weight: 500;
  margin-bottom: 30px;
  text-align: center;
}

.landing-section__button {
  color: white;
  background-color: transparent;
  border: 1px solid white;
  padding: 5px 20px;
}

@media only screen and (max-width: 1024px) {
  .landing-section {
    padding: 60px;
  }
}

@media only screen and (max-width: 768px) {
  .landing-section {
    padding: 20px;
  }

  .landing-section__title {
    font-size: 1rem;
  }

  .landing-section__description {
    font-size: 14px;
  }
}
</style>