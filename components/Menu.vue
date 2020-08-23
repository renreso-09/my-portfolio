<template>
  <div class="menu">
    <div class="menu-contents">
      <div class="menu-item">
        <nuxt-link v-scroll-to="'#profile'" to class="menu-link">
          <img src="../assets/icons/human.svg"/>
          PROFILE
        </nuxt-link>
      </div>
      <div class="menu-item">
        <nuxt-link v-scroll-to="'#skill'" to class="menu-link">
          <img src="../assets/icons/skill.svg"/>
          SKILL
        </nuxt-link>
      </div>
      <div class="menu-item">
        <nuxt-link v-scroll-to="'#work'" to class="menu-link">
          <img src="../assets/icons/folder.svg"/>
          WORK
        </nuxt-link>
        </div>
      <div class="menu-item">
        <nuxt-link v-scroll-to="'#contact'" to class="menu-link">
          <img src="../assets/icons/mail.svg"/>
          CONTACT
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<style>
.menu {
  background-color: #c0c0c0;
}

.menu-contents{
  display: flex;
  justify-content: space-between;
  margin-right: 128px;
  margin-left: 128px;
}

.menu-item {
  font-family: 'Press Start 2P';
  font-weight: bold;
  text-align:center;
  text-decoration: none;
}

.menu-item img {
  width: 32px;
  height: 32px;
}

.menu-link {
  text-decoration: none;
  color: #000;
}
</style>