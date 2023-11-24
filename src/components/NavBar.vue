<template>
  <b-navbar sticky id="navbar-wrapper" toggleable="lg">
    <b-navbar-brand href="#">
      <img
        :src="logo"
        alt=""
        class="navbar-logo"
      >
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav id="navbar-items" class="ml-auto">
        <!-- <b-nav-item href="#" class="navbar-item-link">Program</b-nav-item>
        <b-nav-item href="#" class="navbar-item-link">Kegiatan</b-nav-item> -->
        <!-- <b-nav-item href="#" class="navbar-item-link">Pengajar</b-nav-item> -->
        <b-nav-item href="https://aktlivingacademy.com" class="navbar-item-link-yellow" target="_blank">Pendaftaran Online</b-nav-item>
        <b-nav-item href="https://wa.me/081927088036" class="navbar-item-link" target="_blank">
          <img
            :src="whatsapp"
            alt=""
          >
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
import logo from '@/assets/logo.svg'
import whatsapp from '@/assets/whatsapp.svg'

export default {
  name: 'NavBar',

  data () {
    return {
      logo,
      whatsapp
    }
  }
}
</script>

<style scoped>
#navbar-wrapper {
  background-color: white;
}

#navbar-items {
  align-items: center;
}

.navbar-logo {
  height: 40px;
}

.navbar-item-link {
  font-family: Montserrat;
  color: black;
  font-weight: 500;
  font-size: 14px;
}

.navbar-item-link-yellow {
  border-radius: 45px;
  border: 1px solid rgba(0, 0, 0, 0.00);
  background: #FDBE14;
}

.nav-link {
  padding: 10px !important;
}
</style>
