<template>
	<nav>
		<v-toolbar app dark>
			<v-toolbar-side-icon v-on:click="isDrawerOpen = !isDrawerOpen" />
			<v-toolbar-title>
				<span class="font-weight-black">SOUNDBOARD</span><span class="font-weight-light">APP</span>
			</v-toolbar-title>
		</v-toolbar>

		<v-navigation-drawer dark app v-model="isDrawerOpen">
			<v-list>

				<v-list-tile v-on:click="navigate('/')">
					<v-list-tile-action>
						<v-icon>home</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title>Home</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>

				<v-list-tile v-on:click="navigate('about')">
					<v-list-tile-action>
						<v-icon>info</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title>About</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>

				<v-list-tile v-on:click="navigate('support')">
					<v-list-tile-action>
						<v-icon>live_help</v-icon>
					</v-list-tile-action>
					<v-list-tile-content>
						<v-list-tile-title>Support</v-list-tile-title>
					</v-list-tile-content>
				</v-list-tile>

			</v-list>
		</v-navigation-drawer>
	</nav>
</template>

<script>
export default {
	name: 'Navbar',
	data () {
		return {
			isDrawerOpen: false
		}
	},
	methods: {
		navigate: function (route) {
			this.$router.push(route);
		}
	}
}
</script>

