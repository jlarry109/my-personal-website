<template>
	<div id="home">
		<div style="width: 100%; margin-top: 40px;text-align: center;font-size: 64px;">Larry.Jones</div>
		<div style="height: 1px; background-color:aquamarine;width: 100%;"></div>
		<div style="display: flex;justify-content: center;">
			<div class="button" style="padding-right: 20px;cursor: pointer;" @click="cur=1;">home</div>
			<div class="button" style="padding-right: 20px;cursor: pointer;" @click="cur=2;">CV</div>
			<div class="button" style="padding-right: 20px;cursor: pointer;" @click="cur=3;">contact</div>
		</div>
		<div class="home">
			<div :class="{pic: true, pic1: cur==1, pic2: cur==2, pic3: cur==3}" style="margin: 40px 20px 20px 60px;"></div>
			<div style="width: 50%;margin: 60px 60px 20px 20px; text-align: justify;">
				<div style="font-size: 20px; text-align: center; font-size: 32px;font-weight: bold;">Welcome to My
					Academic Journey</div>
				<div v-show="cur==1" style="font-size: 20px;margin-top: 20px;">Greetings! I am [Your Full Name], a passionate graduate
					student dedicated to
					exploring the intersections of [Your Field of Study]. As a seeker of knowledge and a fervent
					enthusiast
					of [Key Interests or Specializations], I invite you to delve into my academic world. This digital
					space
					serves as a window into my academic pursuits, research endeavors, and the evolving narrative of my
					scholarly journey.</div>
				<div v-show="cur==2" style="font-size: 20px;margin-top: 20px;">Throughout my academic career, I have been driven by a
					deep curiosity to
					understand and contribute to [Central Themes or Research Areas]. Here, you will find an assortment
					of my
					research projects, publications, and reflections, showcasing my commitment to pushing the boundaries
					of
					knowledge in [Your Field]. I believe that academia is not just about individual accomplishments but
					also
					about fostering a collaborative community. As such, I welcome discussions, collaborations, and the
					exchange of ideas with fellow scholars, students, and enthusiasts.
				</div>
				<div v-show="cur==3" style="font-size: 20px;margin-top: 20px;">Feel free to explore the various sections of my webpage
					to gain insights into
					my academic interests, ongoing projects, and the broader impact I aspire to make. Thank you for
					visiting, and I look forward to engaging in meaningful dialogues as we navigate the exciting terrain
					of
					[Your Field] together.
				</div>
				<div style="font-size: 20px;margin-top: 40px;">Best regards,
				</div>
			</div>

			<!-- <div class="button" @click="onAbout()">about</div> -->
		</div>
	</div>
</template>

<script>
	export default {
		data: () => {
			return {
				add: null,
				cur: 1
			}
		},
		mounted() {
			this.add = 0
		},
		methods: {
			onAbout() {
				this.add = this.add + 1
			}
		}
	}
</script>

<style>
	#home {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
	}

	.home {
		margin-top: 60px;
		display: flex;
		justify-content: center;
		/* align-items: center; */
	}

	.pic {
		width: 50%;
		height: 500px;
	}
	
	.pic1 {
		background: url("../assets/pic.jpeg") center/100%;
	}
	
	.pic2 {
		background: url("../assets/logo.png") center/100%;
	}
	
	.pic3 {
		background: url("../assets/pic.jpeg") center/100%;
	}

	.button {
		width: 100px;
		height: 50px;
		text-align: center;
		line-height: 50px;
		color: black;
		user-select: none;
	}

	.button:hover {
		color: aqua;
	}
</style>