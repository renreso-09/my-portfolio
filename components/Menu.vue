<template>
  <div class="menu">
    <div class="menu-contents">
      <div class="menu-item">
        <img src="../assets/icons/human.svg"/>
        <nuxt-link v-scroll-to="'#profile'" to class="menu-link">
          PROFILE
        </nuxt-link>
      </div>
      <div class="menu-item">
        <img src="../assets/icons/skill.svg"/>
        <nuxt-link v-scroll-to="'#skill'" to class="menu-link">
          SKILL
        </nuxt-link>
      </div>
      <div class="menu-item">
        <img src="../assets/icons/folder.svg"/>
        <nuxt-link v-scroll-to="'#work'" to class="menu-link">
          WORK
        </nuxt-link>
        </div>
      <div class="menu-item">
        <img src="../assets/icons/mail.svg"/>
        <nuxt-link v-scroll-to="'#contact'" to class="menu-link">
          CONTACT
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<style>
.menu {
  background-color: #191970;
}

.menu-contents{
  display: flex;
  justify-content: space-between;
  margin-right: 20%;
  margin-left: 20%;
}

.menu-item {
  display: flex;
  justify-content: center;
  align-items: center;
}

.menu-item img {
  width: 3.2rem;
  height: 3.2rem;
  padding: 0.8rem;
}

.menu-link {
  text-decoration: none;
  font-family: 'Press Start 2P';
  font-weight: bold;
  text-align: center;
  text-decoration: none;
  color: rgb(255, 255, 255);
}
</style>