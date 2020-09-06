<template>
  <div class="skill-card">
    <p id="skill-title">NAME: {{skillData.title}}</p>
    <p id="skill-level">Lv: {{skillData.level}}</p>
    <p id="skill-years">YEARS: {{skillData.years}}</p>
    <p id="skill-description">{{skillData.description}}</p>
  </div>
</template>
<script>
  import skillData from '../type/skillData'
  export default {
    props: {
      skillData: skillData
    }
  }
</script>
<style>
.skill-card {
  border-radius: 10px;
  -webkit-border-radius: 10px;  
  -moz-border-radius: 10px;
  background-color: #000000;
}
.skill-card p {
  font-family: 'Press Start 2P';
  color: #ffffff;
  margin-left: 5px;
}
@media (min-width: 1000px){
  .skill-card {
    width: 400px;
    margin: 5px;
  }
}
</style>