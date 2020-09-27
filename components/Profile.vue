<template>
	<div class="profile">
    <div class="profile-image">
      <img src="../static/images/profile_icon.png" alt="profile_icon"/>
    </div>
		<div class="profile-text">
			<p>{{profile.introduction}}</p>
			<p>{{profile.comment}}</p>
			<p>{{profile.language}}</p>
			<p>{{profile.hobby}}</p>
			<p>{{profile.target}}</p>
		</div>
	</div>
</template>
<style>

.profile-text {
	font-family: "Noto Sans JP";
  font-size: 1.4rem;
}
@media only screen and (max-width: 660px){
  .profile-image img {
    width: 60%;
    height: auto;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}
@media only screen and (min-width: 1000px){
  .profile {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .profile-image img {
    width: 256px;
    height: 256px;
  }
}
</style>
<script>
import profile from "../assets/contents/profile.json"
export default {
	data: () => {
		return({profile: profile})
	}
}
</script>