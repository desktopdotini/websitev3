<script context="module">
	export const prerender = true
</script>

<script>
	import Header from '$lib/components/header.svelte'
	import Footer from '$lib/components/footer.svelte'
</script>

<div class="container">
	<Header
		title="Ello! My name is Tanu!"
		desc="I'm a Self-taught Frontend and Backend Developer from Poland!"
		headTitle="Ello! My name is Tanu!"
	/>

	<main>

		<a class="support" href="https://namemc.com/szescdziewiec.3">
			<img src="https://s.namemc.com/img/favicon-128.png" class="love" alt="support" /> My NameMC profile!
		</a>
	</main>
	<Footer />
</div>

<style>

	.support {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;

		width: 100%;
		padding: 1rem;
		margin: 0.5rem 0;

		background: var(--color-primary);
		color: var(--color-on-primary);

		text-align: center;
		text-decoration: none;
		font-weight: bold;
		border-radius: var(--value-radius);
		transition: all 200ms ease;
	}

	.support:hover,
	.support:focus,
	.support:focus-visible {
		background: var(--color-on-primary-contaner);
	}

	.support .love {
		color: var(--color-on-primary);
		width: 1rem;
		height: 100%;
		margin: 0 0.5rem 0 0;
		aspect-ratio: 1/1;
	}
</style>
