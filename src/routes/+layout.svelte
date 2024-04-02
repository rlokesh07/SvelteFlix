<script>

	import '../styles.css';
	import logo from '$lib/images/logo.svg'
	import tmdb from '$lib/images/tmdb.svg'

</script>


<nav>

	<a href="/"><img alt="SvelteFlix" src="{logo}"></a>

	<div class="links">
		<a href="/search">search</a>
		<a href="/watchlist">watchlist</a>
		<a href="/login">login</a>
	</div>

</nav>

<main>

	<slot/>

</main>

<footer>
	<p>data provided by <a href="https://developer.themoviedb.org/docs/getting-started">
		<img src="{tmdb}">
	</a></p>

</footer>

<style>

	nav {
			display: flex;
			width: 100%;
			height: 3rem;
			align-items: center;
			justify-content: space-between;
			max-width: var(--column);
			padding: 0 var(--side);
			color: var(--accent);
	}

	a {
			color: inherit;
			text-decoration: none;
	}
	img {
			height: 1rem;
	}
	.links {
			display: flex;
			gap: 1rem;

	}

	footer {
			display: flex;
			justify-content: center;
			height: 5rem;
	}

</style>