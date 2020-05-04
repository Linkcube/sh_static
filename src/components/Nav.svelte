<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
		background: #fffbf6;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}

	img {
		height: 20px;
	}

	.left {
			float: left;
	}

	.right {
		float: right;
	}

	@media (max-width: 900px) {
	}

	@media (min-width: 900px) {
		ul {
			margin-left: 25%;
			margin-right: 25%;
		}
	}
</style>

<nav>
	<ul>
		<li class="left"><a aria-current='{segment === undefined ? "page" : undefined}' href='.'><img alt="Scanlation Harmonia" src="/full_text_h.png"></a></li>
		<!-- <li class="left"><a aria-current='{segment === "features" ? "page" : undefined}' href='features'>features</a></li>
		<li class="left"><a aria-current='{segment === "about" ? "page" : undefined}' href='about'>about</a></li> -->

		<li class="right"><a href='https://github.com/Linkcube/Scanlation-Harmonia/releases'>download</a></li>
		<li class="right"><a href='https://github.com/Linkcube/Scanlation-Harmonia/'>github</a></li>
	</ul>
</nav>
