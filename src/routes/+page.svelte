<script lang="ts">
	import { base } from "$app/paths";

	const currentYear: string = new Date().getFullYear().toString();
</script>

<div class="left"><p></p></div>
<div class="main">
	<div class="image-container">
		<img
			src="{base}/images/me.jpg"
			alt="Robert Nickel, lächelnd"
			width="100%"
		/>
		<div class="image-text-slogan">
			<h1 style="margin-bottom: 0;">Ich helfe Teams dabei, Software</h1>
			<h1
				style="text-decoration-line: underline; margin-top: 0; margin-bottom: 0;"
			>
				nachhaltig
			</h1>
			<h1 style="margin-top: 0;">zu entwickeln.</h1>
		</div>
		<div class="image-text-name">
			<!-- svelte-ignore a11y-missing-attribute -->
			<img src="{base}/images/arrow.svg" />
			<h3 style="margin-left: 1em;">Robert Nickel</h3>
		</div>
	</div>
	<div class="text-container">
		<p class="smaller">
			Bedeutungsvolle Produkte zu erschaffen erfordert mehr als gute
			Planung.
		</p>

		<p class="why-agile">
			Es erfordert einen Prozess, der auf den <a
				href="https://agilemanifesto.org"
				target="_blank">agilen Werten und Prinzipien</a
			>
			basiert, so dass die Anpassung an eine sich ständig verändernde Umwelt
			nicht nur ein notwendiges Übel ist,<br /> sondern der Schlüssel, um sich
			vom Markt abzusetzen.
		</p>

		<div
			style="margin-top: 2em; padding-left: 2em; border-left: 8px solid rgb(255,255,0"
		>
			Ich bin hauptberuflich Agile Coach in Konstanz,<br />
			zertifizierter Scrum Master (<a
				href="https://www.credly.com/badges/1ac44c66-94cd-4ef6-97b6-6b57af7be3a5"
				target="_blank"
			>
				PSM I</a
			>
			und
			<a
				href="https://www.credly.com/badges/282114d5-732c-407b-8536-e0aac28dac6d"
				target="_blank">PSM II</a
			>),<br />
			habe einen Master in Informatik,<br />
			war vormals Software Engineer (> 5 Jahre) und bin<br />
			(sehr bald) durch die Haufe Akademie zertifizierter
			<a href="https://www.haufe-akademie.de/34218" target="_blank"
				>Systemischer Business Coach</a
			>.
		</div>

		<p class="smaller" style="margin-bottom: 2em;">
			<a
				href="mailto:rn30@robertnickel.online?subject=Hello&body=I%20wanted%20to%20reach%20out..."
				>Schick mir eine E-Mail.</a
			>
		</p>

		<hr style="margin-top: 6em;" />
		<p>© Robert Nickel {currentYear} | <a href="/en">english version</a></p>
	</div>
</div>
<div class="right"><p></p></div>

<style>
	.text-container {
		margin-top: 2em;
		padding-left: 0.5em;
		padding-right: 0.5em;
	}
	.image-container {
		position: relative;
		text-align: center;
		color: white;
	}
	img {
		max-width: 100%;
		height: auto;
	}
	.image-text-slogan {
		position: absolute;
		bottom: 100px;
		width: 200px;
		left: 30%;
		text-align: left;
		transform: translate(-50%, 0);
	}
	.image-text-name {
		display: flex;
		position: absolute;
		font-size: small;
		width: 20px;
		top: 20%;
		right: 25%;
		color: rgb(255, 255, 0);
		transform: translate(50%, 0);
	}

	.left,
	.right {
		float: left;
		width: 25%;
	}
	.main {
		float: left;
		width: 50%;
	}

	@media screen and (max-width: 1200px) {
		.left,
		.main,
		.right {
			width: 100%;
		}
		.container {
			margin-top: 2em;
		}
	}

	h1 {
		font-size: 2rem;
		line-height: 1.3em;
	}

	@media (min-width: 500px) {
		h1 {
			font-size: 3rem;
		}
		.image-text-name {
			font-size: medium;
			width: 100px;
		}
	}

	@media (min-width: 1200px) {
		h1 {
			font-size: 4rem;
			line-height: 1.3em;
		}

		.image-text-name {
			font-size: large;
			top: 20%;
			right: 25%;
		}
	}

	a {
		color: black;
	}

	.why-agile {
		font-size: x-large;
	}

	.smaller {
		margin-top: 2em;
		font-size: large;
	}
</style>
