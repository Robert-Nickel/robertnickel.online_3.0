<div class="container">
	<slot />
</div>

<style>
	.container {
		line-height: 1.5;
		font-family: "LeagueSpartanRegular";
		margin: auto;
	}
	
	@font-face {
		font-family: "LeagueSpartanRegular";
		font-style: Black;
		font-weight: 500;
		src: url("/fonts/LeagueSpartan-Regular.ttf") format("truetype");
	}

	@font-face {
		font-family: "LibreBaskervilleRegular";
		font-style: Black;
		font-weight: 500;
		src: url("/fonts/LibreBaskervill-Regular.ttf") format("truetype");
	}
</style>
