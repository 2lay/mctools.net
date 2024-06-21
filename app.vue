<template>
	<div class="nav">
		<a class="title">McTools.net</a>
		<a class="nav-hover active" href="#home">home</a>
		<a class="nav-hover" href="#home">home</a>
		<a class="nav-hover" href="#home">home</a>
		<a class="nav-hover" href="#home">home</a>
	</div>
	<div style="display: contents">
		<div class="h-screen flex sm:flex-row sm:justify-center overflow-y-auto">
			<main style="margin-top:auto;margin-bottom:auto">
				<NuxtPage :key="$route.fullPath" />
			</main>
		</div>
	</div>
</template>

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

	--primary: hsl(var(--primary-h), var(--primary-s), var(--primary-l));
	--secondary: hsl(var(--secondary-h), var(--secondary-s), var(--secondary-l));
	--danger: hsl(var(--danger-h), var(--danger-s), var(--danger-l));

	--border: hsla(0, 0%, 31%, 1);
	--card: hsla(0, 0%, 0%, 0.7);
	--card-active: hsla(0, 0%, 0%, 0.5);
}

/* base */
body {
	background: #1f1f1f url('/noise.png');
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
	font-size: 1rem !important;
	font-weight: 100 !important;
	color: #e1e1e1;
	text-decoration: none;
}



/* navigation */
.topnav,
.nav {
	overflow: hidden;
}

.nav a {
	float: left;
	color: #f2f2f2;
	text-align: center;
	padding: 14px 16px;
	font-size: 17px;
	transition: 0.3s;
}

.nav .title {
	font-weight: 900 !important;
}

.nav-hover:hover {
	color: hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) + 15%));
}

.nav a.active,
.nav-link.active {
	color: var(--primary);

}

/* colors */
.primary,
.danger {
	box-shadow: 0px 0px 10px var(--card);
}

.primary {
	background-color: var(--primary);
}

.danger {
	background-color: var(--danger);
}

.primary:hover,
.danger:hover {
	box-shadow: 0px 0px 10px hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) + 3%));
	background-color: hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) + 3%));
}

.primary:active,
.danger:active {
	box-shadow: 0px 0px 10px hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) - 3%));
	background-color: hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) - 3%));
}

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
		max-width: 800px;
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

/* styles */
button,
textarea {
	border-radius: 9px;
	font-size: 16px;
	transition: background-color 0.2s, transform 0.05s, box-shadow 0.1s, border 0.2s;
	outline: none;
}

button {
	border: none;
	color: white;
	padding: 5px 15px;
	border-radius: 9px;
	text-align: center;
	text-decoration: none;
	display: inline-block;
	font-size: 18px;
	transition: background-color 0.2s, transform 0.05s, box-shadow 0.1s;
}

button:active {
	transform: scale(0.95);
}

textarea {
	border: 1px solid #252529;
	color: white;
	background-color: #161618;
	padding: 5px 15px;
}

textarea:focus {
	border-color: var(--primary);
}
</style>