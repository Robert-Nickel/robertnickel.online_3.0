<script lang="ts">
	import { base } from '$app/paths';

	const currentYear: string = new Date().getFullYear().toString();
</script>

<div class="container">
	<div class="left"><p /></div>
	<div class="main">
		<div class="image-container">
			<img src="{base}/images/me.jpg" alt="Robert Nickel, smiling" width="100%" />
			<div class="image-text-slogan">
				<h1 style="margin-bottom: 0;">Helping teams to build and deliver software</h1>
				<h1 style="text-decoration-line: underline; margin-top: 0;">sustainably</h1>
			</div>
			<div class="image-text-name">
				<!-- svelte-ignore a11y-missing-attribute -->
				<img src="{base}/images/arrow.svg" />
				<h3 style="margin-left: 1em;">Robert Nickel</h3>
			</div>
		</div>
		<div class="text-container">
			<p class="why-agile">
				Building purposeful digital products requires more than good planning.<br />It requires a
				process that is based on
				<a href="https://agilemanifesto.org" target="_blank">agile values and principles</a>, so
				that adapting to changing requirements in an everchanging world isn't just a necessity,<br
				/>
				but the key advantage over your competition.
			</p>

			<div style="margin-top: 2em; padding-left: 2em; border-left: 8px solid rgb(255,255,0">
				I am an Agile Coach in Constance, Germany,<br />
				Professional Scrum Master (<a
					href="https://www.credly.com/badges/1ac44c66-94cd-4ef6-97b6-6b57af7be3a5"
					target="_blank"
				>
					PSM I</a
				>
				and
				<a href="https://www.credly.com/badges/282114d5-732c-407b-8536-e0aac28dac6d" target="_blank"
					>PSM II</a
				>),<br />
				experienced Software Engineer (6+ years),<br />
				Master of Computer Science,<br />
				and have worked with Scrum since 2016.
			</div>

			<p class="cta">
				If you want my help adopting agile values and principles in your company,<br />
				just <a href="https://calendly.com/robertnickel/30min">give me a call.</a>
			</p>
			<hr />

			<p>© Robert Nickel {currentYear}</p>
		</div>
	</div>
	<div class="right"><p /></div>
</div>

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

	.container {
		margin-top: 0em;
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

	.cta {
		margin-top: 2em;
		margin-bottom: 6em;
		font-size: large;
	}
</style>
