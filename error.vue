<template>
	<div class="nav">
		<a class="title">
			<svg-icon type="mdi" :path="path"></svg-icon> <span class="text">McTools.net</span>
		</a>
		<div class="nav-links">
			<nuxt-link to="/" class="nav" exact-active-class="active">home</nuxt-link>
			<nuxt-link to="/tools" class="nav" exact-active-class="active">tools</nuxt-link>
			<nuxt-link to="/contact" class="nav" exact-active-class="active">contact</nuxt-link>
		</div>
	</div>
	<main>
		<mct-card cardMW="300px" class="card">
			<div style="text-align: center;">
				<h1>404</h1>
				<hr>
				<p style="margin-top: 10px;">This page doesn't exist</p>
				<Nuxt-Link href="/">
					<mct-button style="margin-top: 15px;" icon-name="mdiHome" label="Home" class="mct-button-primary" />
				</Nuxt-Link>
			</div>
		</mct-card>
	</main>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiMinecraft } from '@mdi/js';

export default {
	components: {
		SvgIcon
	},
	data() {
		return {
			path: mdiMinecraft,
		}
	}
}
</script>