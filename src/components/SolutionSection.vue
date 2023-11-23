<template>
  <div class="solution-section">
    <div class="solution-section__wrapper container">
      <div class="solution-section__left">
        <div class="solution-section__subtitle">
          Bantu Anak Anda Jadi Public Speaker Handal Dengan
        </div>
        <div class="solution-section__title">
          Kursus Public Speaking AKT Untuk Anak & Remaja
        </div>
        <div class="solution-section__description">
          Kursus Public Speaking AKT dirancang secara sistematis untuk membantu anak Anda mengembangkan keterampilan komunikasi, presentasi, dan membangun kepercayaan diri bicara di depan umum
        </div>
      </div>
      <img
        :src="classSituation"
        alt=""
        class="solution-section__image"
      >
    </div>
  </div>
</template>

<script>
import classSituation from '@/assets/solution-img.png'

export default {
  name: 'SolutionSection',

  data () {
    return {
      classSituation
    }
  }
}
</script>

<style scoped>
.solution-section {
  background: #483735;
  padding: 80px;
}

.solution-section__wrapper {
  background: #FFC93D;
  display: flex;
  margin: auto;
  padding: 0 !important;
}

.solution-section__left {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 50px;
}

.solution-section__subtitle {
  color: #000;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 700;
  margin-bottom: 30px;
}

.solution-section__title {
  color: #000;
  font-family: Montserrat;
  font-size: 24px;
  font-weight: 900;
  margin-bottom: 20px;
}

.solution-section__description {
  color: #000;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 400;
}

.solution-section__image {
  width: 50%;
  object-fit: cover;
}

@media only screen and (max-width: 1024px) {
  .solution-section__left {
    padding: 30px 50px;
  }
}

@media only screen and (max-width: 768px) {
  .solution-section {
    padding: 40px;
  }

  .solution-section__wrapper {
    flex-wrap: wrap-reverse;
  }

  .solution-section__image {
    width: 100%;
  }

  .solution-section__left {
    padding: 20px;
  }

  .solution-section__title {
    font-size: 1.2rem;
  }
}
</style>