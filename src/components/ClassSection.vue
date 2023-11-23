<template>
  <div class="class-section">
    <div class="class-section__wrapper container">
      <div class="class-section__title">
        2 Kelas Sesuai Minat Anak Anda
      </div>
      <div class="class-section__subtitle">
        Kami membagi Kursus Public Speaking AKT jadi 4 kelas berbeda sesuai bakat dan minat anak Anda
      </div>

      <div class="class-section__classes">
        <div
          v-for="cls in classes"
          :key="cls.title"
          class="class-section__class"
        >
          <div class="class-section__ellipse">
            <img
              :src="cls.image"
              alt=""
              class="class-section__class-image"
            >
          </div>
          <div class="class-section__class-title">
            {{ cls.title }}
          </div>
          <div
            v-for="description in cls.descriptions"
            :key="description"
            class="class-section__class-descriptions"
          >
            <img
              :src="ellipse"
              alt=""
              class="class-section__class-ellipse"
            >
            <div class="class-section__class-description">
              {{ description }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ellipse from '@/assets/ellipse.svg'
import beginner from '@/assets/public-speaking-beginner.png'
import advance from '@/assets/public-speaking-advance.png'

export default {
  name: 'SkillsSection',

  data () {
    return {
      classes: [
        {
          image: beginner,
          title: 'Public Speaking Beginner',
          descriptions: [
            'Belajar tampil percaya diri saat bicara di depan umum',
            'Belajar teknik vokal dan ekspresi suara',
            'Belajar teknik gesture',
            'Belajar mempengaruhi massa'
          ]
        },
        {
          image: advance,
          title: 'Public Speaking Advance',
          descriptions: [
            'Belajar memengaruhi menggunakan paparan',
            'Belajar memengaruhi menggunakan narasi',
            'Belajar memengaruhi menggunakan persuasi',
            'Belajar memengaruhi menggunakan sugesti'
          ]
        }
      ],
      ellipse
    }
  }
}
</script>

<style scoped>
.class-section {
  padding: 80px;
  background: #FDBE14;
}

.class-section__wrapper {
  margin: auto;
}

.class-section__title {
  color: #000;
  text-align: center;
  font-family: Montserrat;
  font-size: 28px;
  font-weight: 900;
  margin-bottom: 40px;
}

.class-section__subtitle {
  color: #000;
  text-align: center;
  font-family: Montserrat;
  font-weight: 500;
  margin-bottom: 60px;
}

.class-section__classes {
  display: flex;
  justify-content: center;
  gap: 50px;
}

.class-section__class {
  border-radius: 31px;
  background: #DFA711;
  padding: 25px;
}

.class-section__ellipse {
  margin: auto;
  padding: 5px;
  background-color: white;
  border-radius: 50%;
  width: 90px;
}

.class-section__class-title {
  margin-top: 50px;
  margin-bottom: 30px;
  color: #000;
  font-family: Montserrat;
  text-align: center;
  font-size: 16px;
  font-weight: 900;
}

.class-section__class-descriptions {
  display: flex;
  gap: 10px;
  margin-bottom: 10px;
}

.class-section__class-description {
  color: #000;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 400;
}

@media only screen and (max-width: 768px) {
  .class-section {
    padding: 30px;
  }

  .class-section__classes {
    flex-wrap: wrap;
  }  
}
</style>