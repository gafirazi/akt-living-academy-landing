<template>
  <div class="risk-section container">
    <img
      :src="person"
      alt=""
      class="risk-section__image"
    >
    <div class="risk-section__right">
      <div class="risk-section__description">
        5 perilaku di atas adalah tanda anak Anda ga punya keberanian tampil di depan umum. Anak Anda belum punya skill public speaking yang sangat dibutuhkan di masa depan. Kalau terus dibiarkan, anak Anda sangat berpotensi jadi bagian dari:
      </div>
      <div
        v-for="description in descriptions"
        :key="description"
        class="risk-section__list-item"
      >
        <img
          :src="ellipse"
          alt=""
        >
        <div class="risk-section__list-description">
          {{ description }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ellipse from '@/assets/ellipse.svg'
import person from '@/assets/risk-img.png'

export default {
  name: 'RiskSection',

  data () {
    return {
      descriptions: [
        'Lebih dari 70% populasi dunia pengidap Glossophobia yang takut bicara di depan umum',
        'Lebih dari 15 juta orang Indonesia yang harus merasakan Glossophobia setiap hari',
        'Lebih dari 85% manusia yang mengalami rasa malu setiap hari'
      ],
      person,
      ellipse
    }
  }
}
</script>

<style scoped>
.risk-section {
  width: 70%;
  margin: 60px auto;
  border-radius: 59px;
  display: flex;
  flex-wrap: wrap;
  background: #F5F5F5;
}

.risk-section__image {
  width: 300px;
}

.risk-section__right {
  display: flex;
  width: 50%;
  flex-direction: column;
  justify-content: center;
  padding-top: 20px;
  padding-right: 20px;
  padding-bottom: 20px;
}

.risk-section__description {
  color: #000;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 700;
  margin-bottom: 30px;
}

.risk-section__list-item {
  display: flex;
  gap: 10px;
  align-items: center;
  margin-bottom: 10px;
}

.risk-section__list-description {
  color: #000;
  font-family: Montserrat;
  font-size: 12px;
  font-weight: 400;
}

@media only screen and (max-width: 900px) {
  .risk-section {
    justify-content: center;
  }

  .risk-section__right {
    width: 90%;
    margin: auto;
  }
}

@media only screen and (max-width: 768px) {
  .risk-section {
    width: 80%;
  }

  .risk-section__image {
    width: 250px;
  }
}
</style>