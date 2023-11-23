<template>
  <div class="contact-us-section">
    <div class="contact-us-section__wrapper container">
      <div class="contact-us-section__title">
        Ga ada kata terlalu dini untuk membantu anak kesayangan Anda pintar bicara di depan umum dengan efektif dan penuh keyakinan. Ga ada kata rugi untuk berinvestasi dalam membangun skill public speaking-nya
      </div>
      <div class="contact-us-section__whatsapp-wrapper">
        <img
          :src="whatsapp"
          alt=""
          class="contact-us-section__whatsapp-logo"
        >
        <a
          href="https://wa.me/081927088036"
          target="_blank"
        >
          <div class="contact-us-section__whatsapp-text">
            WHATSAPP US
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import whatsapp from '@/assets/whatsapp.svg'

export default {
  name: 'ContactUsSection',

  data () {
    return {
      whatsapp
    }
  }
}
</script>

<style scoped>
.contact-us-section {
  padding: 80px;
}

.contact-us-section__wrapper {
  margin: auto;
}

.contact-us-section__title {
  color: #000;
  text-align: center;
  font-family: Montserrat;
  font-size: 20px;
  font-style: normal;
  font-weight: 900;
  line-height: normal;
  margin-bottom: 30px;
}

.contact-us-section__whatsapp-wrapper {
  border-radius: 34.5px;
  width: fit-content;
  height: 35px;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 60px;
  padding-right: 40px;
  background: black;
  position: relative;
}

.contact-us-section__whatsapp-logo {
  position: absolute;
  top: -5px;
  left: -20px;
}

.contact-us-section__whatsapp-text {
  color: #FFF;
  text-align: center;
  font-family: Montserrat;
  font-size: 12px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

@media only screen and (max-width: 768px) {
  .contact-us-section {
    padding: 30px;
  }

  .contact-us-section__title {
    font-size: 1rem;
  }
}
</style>