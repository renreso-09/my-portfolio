<template>
  <div class="portfolio">
    <MobileMenu v-if="screenWidth < 660"/>
    <div class="title">
      <p class="title-text">Ren Hirakawa's Portfolio</p>
    </div>
    <Menu v-if="screenWidth >= 660"/>
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
    <div class="footer">
      <footer>
        <p>©2020 renreso</p>
      </footer>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Menu from '../components/Menu.vue'
import MobileMenu from '../components/MobileMenu.vue'

export default Vue.extend({
  components: {
    Menu,
    MobileMenu
  },
  data(){
    return {
      screenWidth: window.innerWidth,
      screenHeight: window.innerHeight,
    }
  },
   methods: {
    getWindowSize: function() {
      this.screenWidth = window.innerWidth;
      this.screenHeight = window.innerHeight;
    }
  },

  mounted() {
    window.addEventListener('resize', this.getWindowSize);
  },
})
</script>

<style>
.portfolio {
  min-height: 100vh;
  position: relative;
  padding-bottom: 35px;
  box-sizing: border-box;
}
.title {
  display: flex;
  justify-content: center;
}

.title-text {
  width: 24em;
  font-family: 'Press Start 2P';
  font-size: 1vmax;
  text-align: center;
  font-weight: bold;
  border-right: 2px solid rgba(255,255,255,.75);
}

/*1000px以上でアニメーション適用*/ 
@media (min-width: 1000px){
    .title-text {
      overflow: hidden;
      white-space: nowrap;
      animation:
        typewriter 2s steps(30) 1s 1 normal both,
        blinkTextCursor 500ms steps(44) infinite normal; 
    }
  }

@keyframes typewriter{
  from{width: 0;}
}
@keyframes blinkTextCursor{
  from{border-right-color: rgba(0, 0, 2, 0.75);}
  to{border-right-color: transparent;}
}

.footer {
  background-color: #191970;
  color: #ffffff;
  text-align: center;
  position: absolute;
  bottom: 0;
  width: 100%;
}

.contents {
  margin-left: 128px;
  margin-right: 128px;
}

.contents-title {
  font-family: 'Press Start 2P';
  text-align: center;
}
</style>
