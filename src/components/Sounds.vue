<template>
	<v-container fluid grid-list-lg>
		<v-layout wrap>
			<v-flex xs4 v-for="(sound, index) in sounds" :key="index">
				<v-card v-on:click="play(sound.sound)">
					<v-card-text>
						<v-icon color="yellow" x-large>play_arrow</v-icon>
						<p>{{ sound.title }}</p>
					</v-card-text>
				</v-card>
			</v-flex>
		</v-layout>
	</v-container>
</template>

<script>
export default {
	name: 'Sounds',
	data () {
		return {
			sounds: [
				{
					title: "Cow",
					sound: "cow.mp3"
				},
				{
					title: "Bell",
					sound: "bell.mp3"
				},
				{
					title: "Explosion",
					sound: "explosion.mp3"
				},
				{
					title: "Ambulance",
					sound: "ambulance.mp3"
				},
				{
					title: "Bullet",
					sound: "bullet.mp3"
				},
				{
					title: "Fizzle",
					sound: "fizzle.mp3"
				},
				{
					title: "Movie",
					sound: "movie.mp3"
				},
				{
					title: "Punch",
					sound: "punch.mp3"
				},
				{
					title: "Telephone",
					sound: "telephone.mp3"
				}
			]
		}
	},
	methods: {
		play: function (name) {
			let audio = new Audio(require('@/assets/sounds/' + name));
			audio.play();
		}
	}
}
</script>

