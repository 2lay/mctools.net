<template>
		<mct-card cardMW="800px">
			<h1 style="text-align: center; margin-bottom: 15px;">MOTD Creator</h1>
			<div style="text-align: center;">
				<p>Text color</p>
				<div style="margin-top: 10px;">
					<button class="motd-shared motd-color-btn" style="background-color: #000000"></button>
					<!-- Black -->
					<button class="motd-shared motd-color-btn" style="background-color: #0000AA"></button>
					<!-- Dark Blue -->
					<button class="motd-shared motd-color-btn" style="background-color: #00AA00"></button>
					<!-- Dark Green -->
					<button class="motd-shared motd-color-btn" style="background-color: #00AAAA"></button>
					<!-- Dark Aqua -->
					<button class="motd-shared motd-color-btn" style="background-color: #AA0000"></button>
					<!-- Dark Red -->
					<button class="motd-shared motd-color-btn" style="background-color: #AA00AA"></button>
					<!-- Dark Purple -->
					<button class="motd-shared motd-color-btn" style="background-color: #FFAA00"></button> <!-- Gold -->
					<button class="motd-shared motd-color-btn" style="background-color: #AAAAAA"></button> <!-- Gray -->
					<button class="motd-shared motd-color-btn" style="background-color: #555555"></button>
					<!-- Dark Gray -->
					<button class="motd-shared motd-color-btn" style="background-color: #5555FF"></button> <!-- Blue -->
					<button class="motd-shared motd-color-btn" style="background-color: #55FF55"></button>
					<!-- Green -->
					<button class="motd-shared motd-color-btn" style="background-color: #55FFFF"></button> <!-- Aqua -->
					<button class="motd-shared motd-color-btn" style="background-color: #FF5555"></button> <!-- Red -->
					<button class="motd-shared motd-color-btn" style="background-color: #FF55FF"></button>
					<!-- Light Purple -->
					<button class="motd-shared motd-color-btn" style="background-color: #FFFF55"></button>
					<!-- Yellow -->
					<button class="motd-shared motd-color-btn" style="background-color: #FFFFFF"></button>
					<!-- White -->
				</div>
				<p>Text formatting</p>
				<div style="margin-top: 10px;">
					<button class="motd-shared motd-format-btn" style="font-weight: bold;">Bold</button>
					<button class="motd-shared motd-format-btn" style="text-decoration: underline;">Underline</button>
					<button class="motd-shared motd-format-btn" style="font-style: italic;">Italic</button>
					<button class="motd-shared motd-format-btn"
						style="text-decoration: line-through;">Strikethrough</button>
					<button class="motd-shared motd-format-btn">Obfuscated</button>
					<button class="motd-shared motd-format-btn">Reset</button>
				</div>
				<div style="margin-top: 20px;">
					<mct-text-area taPlaceholder="Input your MOTD" taRows="2" maxRows="2"
						taHardLimit=true></mct-text-area>
				</div>
			</div>
		</mct-card>
</template>

<script>
export default {
	name: 'MOTDCreator',
}
</script>

<style scoped>
.motd-shared {
	border: none;
	color: white;
	cursor: pointer;
	border-radius: 5px;
	margin: 0 5px;
	font-size: 16px;
	outline: none;
	transition: background-color 0.3s ease;
	margin-bottom: 10px;
	border: 1px solid #252529;
	background-color: #1e1e21;
}

.motd-color-btn {
	padding: 15px 15px;
}

.motd-format-btn {
	padding: 10px 10px;
}
</style>
