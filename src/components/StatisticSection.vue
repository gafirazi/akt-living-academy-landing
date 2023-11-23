<template>
  <div class="statistic-section">
    <div class="statistic-section__wrapper container">
      <div class="statistic-section__images">
        <!-- <img
          :src="statistic1"
          alt=""
          class="statistic-section__image image-1"
        > -->
        <img
          :src="statistic2"
          alt=""
          class="statistic-section__image image-2"
        >
        <!-- <img
          :src="statistic3"
          alt=""
          class="statistic-section__image image-3"
        > -->
      </div>
      <div class="statistic-section__title">
        1.500+ Orangtua Puas Dengan Cara Kami Mendidik Anak Mereka
      </div>
      <div class="statistic-section__subtitle">
        Pastikan Anak Anda Siap Meraih Sukses di Masa Depan
      </div>
      <div class="statistic-section__description">
        Bekali dia dengan skill fundamental yang dibutuhkan di semua bidang. Pilih kelasnya dan daftarkan anak Anda di Kursus Public Speaking AKT sekarang!
      </div>
    </div>
  </div>
</template>

<script>
import statistic1 from '@/assets/statistic-1.png'
import statistic2 from '@/assets/statistic-2.png'
import statistic3 from '@/assets/statistic-3.png'

export default {
  name: 'StatisticSection',

  data () {
    return {
      statistic1,
      statistic2,
      statistic3
    }
  }
}
</script>

<style scoped>
.statistic-section {
  padding: 80px;
  background: #FDBE14;
}

.statistic-section__wrapper {
  margin: auto;
}

.statistic-section__images {
  display: flex;
  justify-content: center;
}

.statistic-section__title {
  color: #000;
  text-align: center;
  font-family: Montserrat;
  font-size: 40px;
  font-weight: 900;
  margin-top: 50px;
}

.statistic-section__subtitle {
  color: #000;
  text-align: center;
  font-family: Montserrat;
  font-size: 20px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
}

.statistic-section__description {
  margin-top: 30px;
  color: #000;
  text-align: center;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

@media only screen and (max-width: 768px) {
  .statistic-section {
    padding: 30px;
  }

  .image-2 {
    width: 100%;
  }

  .statistic-section__title {
    font-size: 1.5rem;
  }
}
</style>