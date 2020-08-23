<template>
  <div>
    <div class="header">
      <img src="../assets/images/background-image.jpg">
      <p class="main-title">Ren Hirakawa's Portfolio</p>
    </div>
    <Menu />
    <div class="contents">
      <div class="contents-profile" id="profile">
        <p class="contents-title">PROFILE</p>
      </div>
      <div class="contents-skill" id="skill">
        <p class="contents-title">SKILL</p>
      </div>
      <div class="contents-work" id="work">
        <p class="contents-title">WORK</p>
      </div>
      <div class="contents-contact" id="contact">
        <p class="contents-title">CONTACT</p>
      </div>
    </div>
    <div class="footer">footer</div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Menu from '../components/Menu.vue'

export default Vue.extend({
  components: {
    Menu
  }
})
</script>

<style>
.header {
  position: relative;
}

.header p {
  position: absolute;
  color: white;
  top: 50%;
  left: 50%;
  -ms-transform: translate(-50%,-50%);
  -webkit-transform: translate(-50%,-50%);
  transform: translate(-50%,-50%);
  margin:0;
  padding:0;
  font-family: 'Press Start 2P';
  font-weight: bold;
}

.header img {
  width: 100%;
}

.main-title {
   font-size: 2em;
}

.footer {
  background-color: #191970;
}

.contents {
  margin-left: 128px;
  margin-right: 128px;
}

.contents-title {
  font-family: 'Press Start 2P';
}
</style>
