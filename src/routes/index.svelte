<script>
	import { goto } from '@sapper/app';
	import FancyButton from '../components/FancyButton.svelte';
</script>

<style>
	p {
		margin: 0 auto;
		font-size: 18px;
	}

	h2 {
		font-size: 36px;
		font-weight: 500px;
		text-transform: uppercase;
	}

	p {
		margin: 1em auto;
	}

	.main-image {
		padding: 0px;
		margin: 0px;
		background-image: url(/main_page_image.jpg);
		background-position: top;
		background-size: cover;
		background-blend-mode: darken;
	}

	.blok {
		padding-top: 3em;
		padding-bottom: 3em;
		display: flex;
	}

	.description {
		background-color: #92d8f1;
		justify-content: center;
	}

	.description-text {
		color: white;
	}

	.description-image, .series-image{
		margin-top: auto;
		margin-bottom: auto;
	}


	.series-header {
		display: flex;
		justify-content: center;
		text-align: center;
	}

	.series-management {
		flex-direction: column;
	}

	.series-content {
		display: flex;
		flex-direction: row;
		justify-content: center;
	}

	.pink {
		background: pink;
		color: white;
	}

	@media (max-width: 900px) {
		.description-image img {
			margin-left: 0%;
			display: none;
		}

		.main-image {
			height: 300px;
		}

		.description-text {
			text-align: center;
		}

		img {
			width: 100%;
		}
	}

	@media (min-width: 900px) {
		.description-image img {
			margin-left: 100%;
		}

		.main-image {
			height: 600px;
		}

		.description-text {
			text-align: left;
		}
	}

	.series-image img {
			width: 100%;
	}
</style>

<svelte:head>
	<title>Home</title>
</svelte:head>

<div class="main-image"/>

<div class="blok description">
	<div class="description-text">
		<h2>Manage your scanlation <br>projects</h2>
		<p>
			Scanlation Harmonia is an open-source project made to help <br>
			with managing all of the steps of scanlation, <br>
			with a strong emphasis on the translation aspect.
		</p>
		<FancyButton value="Download" on:click={() => goto('https://github.com/Linkcube/Scanlation-Harmonia/releases')}/>
	</div>
	<div class="description-image">
		<img alt="larger logo" src="/favicon.png">
	</div>
</div>

<div class="blok series-management">
	<div class="series-header">
		<h2>Series Management</h2>
	</div>
	<div class="series-header">
		<p>
			Manage configs on a per-series basis, <br>
			with easy access to all of your series <br>
			including a small summary.
		</p>
	</div>
	<div class="series-content">
		<div class="series-image">
			<img alt="series management" src="/series_management.jpg">
		</div>
	</div>
</div>

<div class="blok series-management pink">
	<div class="series-header">
		<h2>Page Control</h2>
	</div>
	<div class="series-header">
		<p>
			Keep track of your dialogues, with boxes for raw and translated content as well as setting the <br>
			intended style and language for the translated content.
			<br>
			<br>
			Easy to select dialogues with both a table and place-able boxes that show <br>
			where the dialogue is on the page.	
		</p>
	</div>
	<div class="series-content">
		<div class="series-image">
			<img alt="series management" src="/page_level.jpg">
		</div>
	</div>
</div>

<!-- <div class="blok series-management">
	<div class="series-header">
		<h2>Browser Driven</h2>
	</div>
	<div class="series-header">
		<p>
			Since this project lives in your browser, it can make use of all the plugins you use for translating.
		</p>
	</div>
</div> -->