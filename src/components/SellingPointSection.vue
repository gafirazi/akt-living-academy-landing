<template>
  <div class="selling-point-section">
    <div class="selling-point-section__wrapper container">
      <div class="selling-point-section__left">
        <img
          :src="puzzle"
          alt=""
          class="selling-point-section__image"
        >
      </div>
      <div class="selling-point-section__right">
        <div class="selling-point-section__title">
          Mengapa Kursus Public Speaking AKT Adalah Pilihan Tepat untuk Anak Anda?
        </div>
        <div
          v-for="sellingPoint in sellingPoints"
          :key="sellingPoint.description"
          class="selling-point-section__list"
        >
          <div class="selling-point-section__list-title">
            {{ sellingPoint.title }}
          </div>
          <div class="selling-point-section__list-description">
            {{ sellingPoint.description }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import puzzle from '@/assets/selling-point-img.png'

export default {
  name: 'SellingPointSection',

  data () {
    return {
      sellingPoints: [
        {
          title: 'Fun',
          description: 'Kami mengemas proses belajar-mengajar dengan suasana yang menyenangkan agar anak Anda ga bosan.'
        },
        {
          title: 'Komprehensif',
          description: 'Kami merancang modul pembelajaran secara komprehensif untuk anak dan remaja sehingga anak Anda lebih mudah memahami dan mempraktekkan setiap materi.'
        },
        {
          title: 'Trainer Profesional',
          description: 'Untuk hasil maksimal, anak Anda akan dibimbing langsung oleh trainer yang punya skill dan pengalaman di dunia public speaking.'
        },
        {
          title: 'Lokasi Strategis',
          description: 'Berlokasi di Kebayoran Baru, mudah diakses dari mana saja.'
        },
        {
          title: 'Kunjungan Ke Stasiun TV',
          description: 'Kami secara rutin mengadakan kunjungan ke stasiun TV untuk membangun mental anak Anda bicara di depan kamera dengan suasana sebenarnya'
        },
      ],
      puzzle
    }
  }
}
</script>

<style scoped>
.selling-point-section {
  padding: 80px;
}

.selling-point-section__wrapper {
  display: flex;
  margin: auto;
  gap: 50px;
}

.selling-point-section__left {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.selling-point-section__title {
  color: #000;
  font-family: Montserrat;
  font-size: 28px;
  font-weight: 900;
  margin-bottom: 40px;
}

.selling-point-section__list-title {
  color: #FFC93D;
  font-family: Montserrat;
  font-size: 20px;
  font-weight: 900;
  margin-bottom: 5px;
}

.selling-point-section__list-description {
  color: #000;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 500;
  margin-bottom: 15px;
}

@media only screen and (max-width: 1024px) {
  .selling-point-section__wrapper {
    flex-wrap: wrap;
    justify-content: center;
    gap: 0px;
  }
}

@media only screen and (max-width: 768px) {
  .selling-point-section__image {
    width: 100%;
  }

  .selling-point-section {
    padding: 30px;
  }

  .selling-point-section__title {
    font-size: 1.5rem;
  }
}
</style>