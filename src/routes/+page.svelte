<script lang="ts">
	const currentYear: string = new Date().getFullYear().toString();
</script>

<div class="container">
	<div class="left"><p /></div>
	<div class="main">
		<h1>Ich helfe Teams dabei, wertschöpfende Software nachhaltig zu entwickeln.</h1>

		<img
			src="/images/ac-se.svg"
			alt="Ein Venn-Diagramm von Agile Coaching und Software Engineering, wo in der Schnittmenge der beiden Kreise 'Hier liegt der Hund begraben' steht."
		/>
		<p>
			Dafür arbeite ich an der Schnittstelle zwischen dem Software Engineering und dem Agile
			Coaching.
		</p>

		<h2>Wer?</h2>
		<p>
			Ich bin Robert Nickel. Durch meine mehrjährigen, praktischen Erfahrungen in beiden Bereichen
			durfte ich lernen, was es bedeutet, Softwaresysteme architektonisch zu planen, produktiven
			Code und Tests zu schreiben, aber auch Scrum einzuführen, agile Prinzipien und Clean Code
			Prinzipien vorzuleben und mit den eigenen Händen qualitativ hochwertige digitale Produkte zu
			entwickeln.
		</p>
		<h2>Für wen?</h2>
		<p>Wenn Ihnen eines dieser folgenden Probleme bekannt vorkommt:</p>
		<ol>
			<li>Die Software hat einfach zu viele Bugs,</li>
			<li>die Entwickler brauchen sehr viel Zeit für Kleinigkeiten,</li>
			<li>
				die Schätzungen sind über einen längeren Zeitraum um Faktor 2 oder mehr daneben, und machen
				die Entwicklung somit völlig unplanbar
			</li>
			<li>sich jedes Release wie ein riskantes Unterfangen anfühlt,</li>
			<li>
				Sprintwechsel ein Tauziehen zwischen zusätzlicher Funktionalität und der Beseitigung von
				technischen Schulden ist,
			</li>
		</ol>
		<p>
			oder Sie sich fragen, warum nicht mehr Leute Ihr Produkt benutzen wollen, dann kann ich Ihnen
			damit helfen!
		</p>

		<h2>Wie genau?</h2>
		<p>
			Ich führe eine systematische, tiefgehende und völlig transparente Analyse der Strukturen Ihrer
			Organisation durch. Mittels einer professionellen Durchleuchtung aller technologischen,
			organisatorischen und kommunikativen Zusammenhänge, finde ich mit Ihnen gemeinsam systematisch
			die größten Verbesserungspotentiale Ihres Unternehmens. Damit steigern Sie nicht nur die
			Zufriedenheit Ihrer Mitarbeiter, sondern auch die Wertschöpfungsfähigkeit Ihres Unternehmens.
		</p>
		<p>
			Als unabhängiger Berater kann ich dabei kritische Bereiche völlig unbefangen und
			interessenskonfliktfrei beschreiten, und ehrliche, klare Einblicke in komplexe Zusammenhänge
			geben. Treten Sie gerne ganz unbefangen in Kontakt mit mir!
		</p>

		<hr />

		<p>© Robert Nickel {currentYear}</p>
	</div>
	<div class="right"><p /></div>
</div>

<style>
	img {
		max-width: 100%;
		height: auto;
	}

	.container {
		margin-top: 8em;
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

	@media screen and (max-width: 1000px) {
		.left,
		.main,
		.right {
			width: 100%;
		}
		.container {
			margin-top: 4em;
			margin-left: 1em;
			margin-right: 1em;
		}
	}
</style>
