<template>
	<div class="profile">
		<p>{{profile.data}}</p>
	</div>
</template>
<style>
.profile {
	text-align: center;
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