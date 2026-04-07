<script lang="ts">
	import { asset } from "$app/paths";
	const currentYear: string = new Date().getFullYear().toString();
</script>

<div class="main">
	<div class="image-container">
		<img
			src={asset("/images/me.jpg")}
			alt="Robert Nickel, lächelnd"
			width="100%"
		/>
		<div class="image-text-slogan">
			<h1 style="margin-bottom: 0;">Rational und empathisch.</h1>
		</div>
		<div class="image-text-name">
			<!-- svelte-ignore a11y-missing-attribute -->
			<img src={asset("/images/arrow.svg")} />
			<h3 style="margin-left: 1em; text-align: left;">Robert Nickel</h3>
		</div>
	</div>
	<div class="text-container">
		<h2><u>Entscheidungscoaching</u> ist mein zentrales Coachingthema</h2>
		<p>
			Durch strukturierte Methoden gewinnst du neue Perspektiven,
			Erkenntnisse über deine Situation, deine eigenen Werte und Optionen.
			Unser gemeinsames Ziel ist die Erlangung der Klarheit, um
			selbstbewusst die richtige Entscheidung zu treffen.
		</p>
		<p>
			Ich bringe bei Bedarf viel Wissen zu typischen Denkfehlern und
			mentalen Verzerrungen (Biases) mit, so dass sich die Entscheidung
			nicht nur richtig anfühlt.
		</p>

		<div
			style="margin-top: 2em; padding-left: 2em; border-left: 8px solid rgb(255,255,0"
		>
			<h2>Ich?</h2>
			...bin zertifizierter Systemischer Business Coach (Haufe Akademie)<br
			/>
			...bin von Haus aus Informatiker (Master of Science)<br />

			...habe Erfahrung in Softwareentwicklung (5 Jahre als Software
			Engineer, 3 Jahre als Agile Coach)
			<br />
			...war schon in einem Konzern (4,5 Jahre), einem Startup (1 Jahr) und
			einem mittelständischen Unternehmen (2,5 Jahre)<br />
			...und lebe und arbeite in Konstanz.
		</div>

		<h2>Weitere Coachinganliegen könnten sein</h2>
		<ul>
			<li>persönliche Weiterentwicklung (Wer will ich sein?)</li>
			<li>Gewohnheitsänderungen (Wie will ich sein?)</li>
			<li>Zielklarheit (Wo will ich hin?)</li>
		</ul>

		<h2>Preistransparenz</h2>
		<p>
			Mein Stundensatz für Privatpersonen beträgt 55€ pro 60 Minuten
			Session, wobei die erste Session kostenlos ist.
		</p>
		<p>
			Für Unternehmen schreibe ich gerne ein maßgeschneidertes Angebot
			nach einer strukturierten Auftragsklärung, welche ebenfalls
			kostenlos ist.
		</p>

		<h2>Wie machen wir das?</h2>

		<p>
			Einfach. Schreib mir eine Mail an <a
				href="mailto:coaching@robertnickel.online"
				>coaching@robertnickel.online</a
			> mit deinem ungefähren Anliegen, dann machen wir ein kostenloses Erstgespräch
			aus.
		</p>
		<p>
			Wir können das Coaching vor Ort in Konstanz oder Umgebung machen,
			oder remote. Beides hat eigene Vor- und Nachteile.
		</p>
		<p>
			Für Unternehmen erstreckt sich der Radius für Vor Ort Besuche auf
			die beiden südlichen Bundesländer sowie die Schweiz.
		</p>

		<hr style="margin-top: 6em;" />
		<p>
			© Robert Nickel {currentYear}
		</p>
	</div>
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

	.main {
		width: 50%;
		margin: 0 auto;
	}

	@media screen and (max-width: 1200px) {
		.main {
			width: 100%;
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
