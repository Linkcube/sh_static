<svelte:head>
	<title>Features</title>
</svelte:head>

<style>
	p {
		font-size: 18px;
		
	}
	.features-container {
		padding-top: 3em;
	}
	.column {
		display: flex;
		flex-direction: column;
	}
	.row {
		display: flex;
		flex-direction: row;
	}
	.header {
		text-align: center;
		justify-content: center;
		padding-top: 1em;
	}
	.around {
		justify-content: space-around;
	}
	.text-bubble {
		background: #92d8f1;
		padding: 2em;
		margin-top: auto;
		margin-bottom: auto;
	}
	.page-text-bubble {
		background: #92d8f1;
		padding: 1em;
		margin-top: auto;
		margin-bottom: auto;
	}
	.series-text-bubble {
		background: white;
		padding: 2em;
		margin-top: auto;
		margin-bottom: auto;
	}
	.pink {
		background: pink;
	}
	.purple {
		background-color: #92d8f1;
	}
	.orange {
		background: white;
	}
	.small {
		margin-top: auto;
		margin-bottom: auto;
	}
	.features {
		background-color: #92d8f1;
		justify-content: center;
		color: white;
		padding: 3em;
	}

	.pink, .purple {
			color: white;
	}

	.orange {
		color: gray;
	}

	@media (max-width: 900px) {
		.text-bubble, .page-text-bubble, .series-text-bubble {
			/* width: 100%; */
			border-radius: 0px;
			background: none;
		}

		.block {
			padding-bottom: 1em;
		}

		.page-block {
			padding: 0;
			padding-bottom: 1em;
			width: 100%;
		}

		.wrap {
			flex-wrap: wrap;
		}

		img {
			/* width: fit-content;
			margin-left: auto;
			margin-right: auto; */
			width: 100%;
		}
	}

	@media (min-width: 900px) {
		.text-bubble, .series-text-bubble {
			width: 30%;
			border-radius: 15px;
		}

		.page-text-bubble {
			border-radius: 15px;
			margin: 1em;
		}

		.text-bubble, .page-text-bubble {
			color: white;
		}

		.series-text-bubble {
			color: gray;
		}
		
		.block {
			padding-top: 1em;
			padding-bottom: 1em;
		}

		.page-block {
			padding: 2em;
			border-radius: 5px;
			width: min-content;
		}

		.wrap {
			flex-wrap: wrap;
		}

		img {
			width: fit-content;
		}
	}
</style>

<div class="features-container column">
	<div class="features header row">
		<h1>Scanlation Harmonia Features</h1>
	</div>

	<div class="header row pink">
		<h1>Page Level</h1>
	</div>

	<div class="row wrap around pink">
		<div class="column page-block">
			<div class="page-text-bubble">
				<p>
					After setting the different image levels, 
					you can change between them to compare.
				</p>
			</div>
			<img alt="view" src="/image_views.gif">
		</div>
		<div class="column page-block">
			<div class="page-text-bubble">
				<p>
					Dialogues have a red box that will be placed 
					on the page, you can use this to indicate what 
					the text contents is refering to.
				</p>
			</div>
			<img alt="view" src="/add_dialogue.gif">
		</div>
		<div class="column page-block">
			<div class="page-text-bubble">
				<p>
					The red dialogue boxes are toggle-able in 
					case you want to view just the image.
				</p>
			</div>
			<img alt="view" src="/toggle_dialogue.gif">
		</div>
	</div>


	<div class="header row orange">
		<h1>Chapter Level</h1>
	</div>

	<div class="column">
		<div class="row wrap around block orange">
			<div class="text-bubble">
				<p>
					The chapter view allows you to import existing pages, as well as export the chapter for uploading. <br>
					The importing function expects a directory of photos that it will sort and copy to new pages. <br>
					Exporting will grab the most finished version of each page, and copy it to a new directory which will be opened upon completion.
				</p>
			</div>
			<div class="small">
				<img alt="view" src="/chapter_view.jpg">
			</div>
		</div>
	</div>

	<div class="header row purple">
		<h1>Series Level</h1>
	</div>

	<div class="column">
		<div class="row wrap around block purple">
			<div class="series-text-bubble">
				<p>
					Tables for both dialogue styles and language settings. <br>
					They both include space for the title of the config, as well as any notes you may have for it (i.e font settings).
				</p>
			</div>
			<img alt="view" src="/style_table.jpg">
		</div>
	</div>
</div>



