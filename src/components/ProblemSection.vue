<template>
  <div class="problem-section">
    <div class="problem-section__wrapper">
      <div class="problem-section__title">
        Anda Lihat Tanda-Tanda Ini Ada Pada Anak Anda?
      </div>
      <div
        v-for="description in descriptions"
        :key="description"
        class="problem-section__list-item"
      >
        <img
          :src="ellipse"
          alt=""
        >
        <div class="problem-section__list-text">
          {{ description }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ellipse from '@/assets/ellipse.svg'

export default {
  name: 'ProblemSection',

  data () {
    return {
      descriptions: [
        'Pendiam dan cenderung introvert',
        'Malu bicara dengan orang baru',
        'Ingin nimbrung dalam obrolan, tapi ga punya keberanian',
        'Sangat gelisah saat berada di panggung atau bicara di depan umum',
        'Ga nyaman saat orang lain menilai kemampuan bicaranya'
      ],
      ellipse
    }
  }
}
</script>

<style scoped>
.problem-section {
  padding: 100px 0;
  color: black;
  background: #FFC93D;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.problem-section__title {
  font-family: Montserrat;
  font-size: 28px;
  font-style: normal;
  font-weight: 900;
  margin-bottom: 20px;
}

.problem-section__list-item {
  display: flex;
  gap: 10px;
  align-items: center;
  margin-bottom: 15px;
}

.problem-section__list-text {
  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
}

@media only screen and (max-width: 768px) {
  .problem-section {
    padding: 40px;
  }

  .problem-section__title {
    font-size: 1.5rem;
  }
}
</style>