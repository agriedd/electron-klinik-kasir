<template>
	<v-app>
		<v-navigation-drawer>
			<v-list>
				<v-list-item>
					<v-list-item-avatar>
						<v-avatar>
							<v-icon>mdi-view-dashboard</v-icon>
						</v-avatar>
					</v-list-item-avatar>
					<v-list-item-content>
						<v-list-item-title>
							Home
						</v-list-item-title>
						<v-list-item-subtitle>
							Dashboard
						</v-list-item-subtitle>
					</v-list-item-content>
				</v-list-item>
			</v-list>
		</v-navigation-drawer>
		<v-main>
			<v-card>
				<v-card-text>{{ counter }}</v-card-text>
			</v-card>
			<v-btn @click="increment">Increment</v-btn>
		</v-main>
	</v-app>
</template>

<script>
export default {
	name: 'App',
	components: {
	},
	computed: {
		counter() {
			return this.$store.state.count;
		}
	},
	data: () => ({
		//
	}),
	methods: {
		increment() {
			this.$store.commit('increment');
		}
	},
}
</script>
