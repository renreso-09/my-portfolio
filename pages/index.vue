<template>
  <div class="portfolio">
    <MobileMenu v-if="screenWidth < 660"/>
    <div class="title-head">
      <div class="title">
        <p class="title-text">Renreso's Portfolio</p>
      </div>
    </div>
    <Menu v-if="screenWidth >= 660"/>
    <div class="contents">
      <div class="contents-profile" id="profile">
        <p class="contents-title">PROFILE</p>
        <Profile />
      </div>
      <div class="contents-skill" id="skill">
        <p class="contents-title">SKILL</p>
        <div class="skill">
          <SkillCard v-for="(data, index) in skillDatas" :key="index" :skillData="data.skill" class="skill-card"/>
        </div>
      </div>
      <div class="contents-work" id="work">
        <p class="contents-title">WORK</p>
        <p class="comming-soon">COMMING SOON...</p>
      </div>
      <div class="contents-contact" id="contact">
        <p class="contents-title">CONTACT</p>
        <a href="https://twitter.com/blacklo46145764" target="_blank" class="contact_twitter">
          <img src="/images/twitter_icon.svg" alt="twitter_icon">
        </a>
      </div>
    </div>
    <div class="footer">
      <footer>
        <p>©2020 renreso</p>
      </footer>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import Menu from '../components/Menu.vue'
import MobileMenu from '../components/MobileMenu.vue'
import Profile from '../components/Profile.vue'
import SkillCard from '../components/SkillCard.vue'
import skillData from '../assets/contents/skill.json'
import WorkCard from '../components/WorkCard.vue'

export default Vue.extend({
  components: {
    Menu,
    MobileMenu,
    Profile,
    SkillCard,
    WorkCard
  },
  data(){
    return {
      screenWidth: window.innerWidth,
      screenHeight: window.innerHeight,
      skillDatas: skillData
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

.title-head {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 95vh;
}

.title {
  display: flex;
  justify-content: center;
}

.title-text {
  width: 19em;
  font-family: 'Press Start 2P';
  font-size: 2.4rem;
  text-align: center;
  font-weight: bold;
  border-right: 2px solid rgba(255,255,255,.75);
}

.comming-soon {
  font-family: 'Press Start 2P';
  font-size: 1.6rem;
  text-align: center;
  font-weight: bold;
}

.contact_twitter {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 16px;
  margin-bottom: 16px;
}
.contact_twitter img {
  width: 6.4rem;
  height: 6.4rem;
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
    .contents {
      margin-left: 128px;
      margin-right: 128px;
    }
    .skill {
      display: flex;
      justify-content: center;
      flex-wrap:wrap;
      margin-left: 256px;
      margin-right: 256px;
    }
    .skill-card {
      width: 40%;
    }
}

/*660px(モバイル対応)未満のCSS*/
@media (max-width: 660px) {
  .contents {
    margin-left: 15%;
    margin-right: 15%;
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

.contents-title {
  font-family: 'Press Start 2P';
  text-align: center;
  font-size: 2.4rem;
}
</style>
