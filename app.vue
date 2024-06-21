<template>
	<div class="nav">
		<a class="title">
			<svg-icon type="mdi" :path="path"></svg-icon> <span class="text">McTools.net</span>
		</a>
		<div class="nav-links">
			<nuxt-link to="/" class="nav-hover active">home</nuxt-link>
			<nuxt-link to="tools" class="nav-hover">tools</nuxt-link>
			<nuxt-link to="contact" class="nav-hover">contact</nuxt-link>
		</div>

	</div>
	<div class="main-content">
		<main>
			<NuxtPage />
		</main>
	</div>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon';
import { mdiMinecraft } from '@mdi/js';

export default {
	name: "my-component",
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


<style>
/* imports */
@import url('https://meyerweb.com/eric/tools/css/reset/reset.css');
@import url('https://fonts.googleapis.com/css2?family=Sintony:wght@400;700&display=swap');

/* root variables */
:root {
	--primary-h: 254;
	--primary-s: 100%;
	--primary-l: 64%;

	--secondary-h: 254;
	--secondary-s: 42%;
	--secondary-l: 22%;

	--danger-h: 348;
	--danger-s: 100%;
	--danger-l: 64%;

	--warning-h: 30;
	--warning-s: 100%;
	--warning-l: 64%;

	--success-h: 145;
	--success-s: 78%;
	--success-l: 48%;

	--primary: hsl(var(--primary-h), var(--primary-s), var(--primary-l));
	--secondary: hsl(var(--secondary-h), var(--secondary-s), var(--secondary-l));
	--danger: hsl(var(--danger-h), var(--danger-s), var(--danger-l));
	--warning: hsl(var(--warning-h), var(--warning-s), var(--warning-l));
	--success: hsl(var(--success-h), var(--success-s), var(--success-l));

	--border: hsla(0, 0%, 31%, 1);
	--card: hsla(0, 0%, 0%, 0.7);
	--card-active: hsla(0, 0%, 0%, 0.5);
}

/* base */
body {
	background: #1b1b1b url('/noise.png');
	box-sizing: border-box;
	pointer-events: none;
}

body * {
	pointer-events: auto;
}

h1,
h2,
p,
a {
	font-family: 'Sintony', sans-serif;
}

h1 {
	font-weight: 700 !important;
	color: #f1f1f1;
}

h2 {
	font-weight: 500 !important;
	color: #f1f1f1;
}

p {
	font-size: 0.9rem !important;
	font-weight: 100 !important;
	color: #e1e1e1;
}

p strong,
a {
	font-weight: 700 !important;
	color: #ffffff;
}

a,
.nav a {
	display: inline-flex;
	font-size: 1rem !important;
	font-weight: 100 !important;
	color: #e1e1e1;
	text-decoration: none;
}

strong {
	font-weight: 900 !important;
}

/* navigation */
.nav {
	overflow: hidden;
	display: flex;
	justify-content: space-between;
	padding: 0.2rem;
}

.nav a {
	color: #929292;
	padding: 16px 16px;
	transition: 0.3s;

}

.nav .title {
	font-weight: 900 !important;
	color: #ffffff !important;
	display: flex;
	align-items: center;
}

.nav-hover:hover {
	color: hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) + 15%));
}

.nav a.active,
.nav-link.active {
	color: var(--primary);

}

/* colors */


/* containers */
.flex {
	display: flex;
	flex-wrap: wrap;
}

main {
	margin: auto;
	padding: 1rem;
	width: 100%;
	box-sizing: border-box;
	max-width: 600px;
}

main * {
	max-width: 100%;
	box-sizing: border-box;
}

/* mobile */
@media (min-width: 940px) {
	main {
		max-width: 1200px;
	}

	h1 {
		font-size: 2.5rem;
		margin-bottom: 4px;
	}

	h2 {
		font-size: 1.5rem;
	}

	.sm\:justify-center {
		justify-content: center;
	}

	.sm\:flex-row {
		flex-direction: row;
	}

	.hide-desktop {
		display: none !important;
	}
}

@media (max-width: 939px) {
	main {
		max-width: 100%;
	}

	h1 {
		font-size: 1.5rem;
	}

	h2 {
		font-size: 1.25rem;
	}

	.hide-mobile {
		display: none !important;
	}
}
</style>
