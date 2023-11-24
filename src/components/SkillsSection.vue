<template>
  <div class="skills-section">
    <div class="skills-section__wrapper container">
      <div class="skills-section__title">
        Apa Saja Yang Akan Dipelajari Anak Anda?
      </div>
      <div class="skills-section__skills">
        <div
          v-for="skill in skills"
          :key="skill.title"
          class="skills-section__skill"
        >
          <div class="skill__ellipse">
            <img
              :src="skill.image"
              alt=""
              class="skill__image"
            >
          </div>
          <div class="skill__title">
            {{ skill.title }}
          </div>
        </div>
      </div>

      <div class="skills-section__other-skills">
        Dan 10+ skills lainnya
      </div>
    </div>
  </div>
</template>

<script>
import speaking from '@/assets/speaking.png'
import leadership from '@/assets/leadership.png'
import like from '@/assets/like.png'
import groupChat from '@/assets/group-chat.png'
import dance from '@/assets/dance.png'
import spirit from '@/assets/spirit.png'

export default {
  name: 'SkillsSection',

  data () {
    return {
      skills: [
        {
          title: 'Skill Komunikasi',
          image: speaking
        },
        {
          title: 'Skill Leadership',
          image: leadership
        },
        {
          title: 'Menyampaikan pendapat dengan jelas',
          image: like
        },
        {
          title: 'Skill mempengaruhi orang lain',
          image: groupChat
        },
        {
          title: 'Skill gesture (bahasa tubuh)',
          image: dance
        },
        {
          title: 'Skill oratorium (berorasi)',
          image: spirit
        }
      ]
    }
  }
}
</script>

<style scoped>
.skills-section {
  padding: 80px;
  background: #FDBE14;
}

.skills-section__wrapper {
  margin: auto;
}

.skills-section__title {
  color: #000;
  font-size: 24px;
  font-weight: 900;
  margin-bottom: 60px;
  text-align: center;
}

.skills-section__skills {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 50px;
  margin-bottom: 80px;
}

.skills-section__skill {
  border-radius: 34.5px;
  height: 65px;
  width: 310px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 60px;
  padding-right: 15px;
  background: #DFA711;
  position: relative;
}

.skill__ellipse {
  border-radius: 50%;
  background-color: white;
  padding: 8px;
  position: absolute;
  top: -5px;
  left: -20px;
}

.skill__title {
  color: #000;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 700;
}

.skill__image {
  width: 59px;
  height: 59px;
  object-fit: contain;
}

.skills-section__other-skills {
  border-radius: 34.5px;
  background: #DFA711;
  margin: auto;
  height: 65px;
  width: 310px;
  color: #000;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Montserrat;
  font-size: 24px;
  font-weight: 500;
}

@media only screen and (max-width: 1024px) {
  .skills-section__skills {
    justify-content: center;
  }
}

@media only screen and (max-width: 768px) {
  .skills-section {
    padding: 40px;
  }

  .skill__title {
    font-size: 14px;
  }
}
</style>