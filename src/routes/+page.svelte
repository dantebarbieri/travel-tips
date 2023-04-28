<script lang="ts">
	import { LOGO_PATH, TEXT_PATH } from './airbnb.paths';
</script>

<svelte:head>
	<!-- Jost -->
	<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Jost" />
	<!-- Karla -->
	<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Karla" />
</svelte:head>

<main>
	<h1>Dante's Travel Advice</h1>
	<article>
		<h2 id="apps">Planning/Organization Apps</h2>
		<summary>
			<section class="pros">
				<ul>
					<li>Automatically captures lodging/tickets from email.</li>
					<li>Easy to access, share, etc.</li>
				</ul>
			</section>
			<section class="cons">
				<ul>
					<li>
						You have to forward it your emails or let it watch everything that comes into your
						inbox.
					</li>
					<li>Manually adding things that aren't detected via email can be painful.</li>
				</ul>
			</section>
		</summary>
		<p>
			I strongly suggest using apps like <a href="https://www.tripit.com/web"
				><img
					class="inline"
					src="https://www.tripit.com/themes/custom/tripit_theme/images/logo-tripit.svg"
					alt="TripIt"
				/></a
			> to organize lodging/tickets. Super helpful especially if you're going to be in a lot of Hostels
			or Airbnbs. Also great for getting to tickets and rail passes quickly.
		</p>
	</article>

	<article>
		<h2 id="luggage-management">Luggage Management</h2>
		<summary>
			<section class="pros">
				<ul>
					<li>Generally available.</li>
				</ul>
			</section>
			<section class="cons">
				<ul>
					<li>Need to contact lodging ahead of time.</li>
				</ul>
			</section>
		</summary>
		<p>
			This is only necessary for trips where you're moving around a lot. If you're going to stay in
			one place for multiple nights, this is not a problem.
		</p>
		<p>
			Double check that all of your lodgings will let you drop luggage there. Hotels are great at
			this, <a href="https://www.airbnb.com/">
				<svg class="inline" viewBox="0 0 102 32" color="#FF385C">
					<path d={LOGO_PATH} fill="currentcolor" /><path d={TEXT_PATH} fill="currentcolor" />
				</svg>
			</a>&rsquo;s vary by host (make sure to ask!), and I don't have as much experience with
			Hostels.
		</p>
	</article>

	<article>
		<h2 id="plan-enough">Plan Enough to Always Have Something To Do</h2>
		<summary>
			<section class="pros">
				<ul>
					<li>You're never at a loss for what to do.</li>
				</ul>
			</section>
			<section class="cons">
				<ul>
					<li>Requires more planning.</li>
				</ul>
			</section>
		</summary>
		<p>
			If you don't plan enough, you'll end up wasting a lot of time trying to figure out what to do.
		</p>
		<p>
			At the same time, minimize commitments. Try to not book things unless you're sure you want to
			do them.
		</p>
		<p>
			I personally find that the best balance is struck when I plan some major things to do and also
			some things that would be fun in the nearby area (e.g. walks, parks, museums, etc.). Then, if
			I have extra time I can do some of the fun things but I never have any intention to do them so
			I don't feel to bad if I don't.
		</p>
	</article>

	<article>
		<h2 id="level-setting">Know All Traveler&rsquo;s Levels</h2>
		<summary>
			<section class="pros">
				<ul>
					<li>You don't get tied down by the slowest traveler.</li>
					<li>You don't get exhausted by the fastest traveler.</li>
				</ul>
			</section>
			<section class="cons">
				<ul>
					<li>You may need to split up your group at times.</li>
				</ul>
			</section>
		</summary>
		<p>
			It is important when trip planning to make sure that everyone's expectations are aligned. My
			brother will be done after a single excursion per day and will also need rest days from time
			to time. My parents, conversely, will want to do multiple things per day and will not want to
			rest. Anjali and I are somewhere in the middle&hellip;
		</p>
	</article>

	<p>&copy; 2023 Dante Barbieri</p>
</main>

<style>
	@media (prefers-color-scheme: dark) {
		main {
			background-color: #272727;
			color: #ffffffc0;
		}
	}

	main {
		scroll-behavior: smooth;
		max-width: 100vw;
		width: 100%;
		min-height: 100vh;
		min-height: 100svh;
		height: 100%;
		padding: 0 1em;
		display: flex;
		flex-direction: column;
		font-family: 'Karla', sans-serif;
	}

	h1,
	h2 {
		font-family: 'Jost', sans-serif;
	}

	article {
		/* color: #808080; */
		background-color: #80808030;
		box-shadow: 0.3em 0.4em 0.3em #80808050;
		border-radius: 0.5em;
		padding: 0.5em;
		transition: box-shadow 0.2s ease-in-out, translate 0.2s ease-in-out;
		margin-bottom: 1.5em;
	}

	article:last-child {
		margin-bottom: 0;
	}

	article:hover,
	article:focus {
		box-shadow: 0.4em 0.5em 0.5em #80808080;
		translate: -0.1em -0.2em;
	}

	article > h2:first-child {
		margin-top: 0;
	}

	article > p:last-child {
		margin-bottom: 0;
	}

	.inline {
		height: 1em;
	}

	summary {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		position: relative;
		margin-top: 3em;
		border-radius: 2em;
	}

	summary::before {
		content: 'Summary';
		position: absolute;
		font-size: larger;
		font-family: 'Jost', sans-serif;
		top: -1.5em;
		z-index: 1;
	}

	summary li {
		padding-left: 0.667em;
	}

	.pros {
		/* background-color: #90ee90aa; */
		background-image: linear-gradient(90deg, #90ee9077 0 90%, transparent 100%);
		border-radius: 0.5em 0 0 0.5em;
		flex-grow: 1;
		max-width: 50%;
	}

	.pros ul {
		list-style-type: '\2705';
	}

	.cons {
		/* background-color: #f08080aa; */
		background-image: linear-gradient(-90deg, #f0808077 0 90%, transparent 100%);
		border-radius: 0 0.5em 0.5em 0;
		flex-grow: 1;
		max-width: 50%;
	}

	.cons ul {
		list-style-type: '\274C';
	}

	a {
		color: dodgerblue;
		border-bottom: 0.1em solid transparent;
		text-decoration: none;
	}

	a:visited {
		color: darkorchid;
	}

	a:hover,
	a:focus {
		border-bottom: 0.1em solid currentColor;
	}
</style>
