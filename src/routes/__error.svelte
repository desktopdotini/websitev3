<script context="module">
	/** @type {import('@sveltejs/kit').ErrorLoad} */
	export function load({ error, status }) {
		return {
			props: {
				status: status,
				error: error.message
			}
		}
	}
</script>

<script>
	export let status
	export let error
</script>

<title>Oops! Error {status}</title>

<div class="container">
	<div class="center">
		<div class="error">
			<div class="dialog">
				<h1>Well, something went wrong...</h1>
				<p>
					Error code: {status} <br />
					What happened: {error}
				</p>
			</div>
			<a href="/">Take me back home!</a>
		</div>
	</div>
</div>

<style>
	.center {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.error {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		justify-content: space-between;
		background: var(--color-tertiary);
		border-radius: var(--value-radius);
		color: var(--color-on-tertiary);
		width: 100%;
		margin: 1em 1em;
		padding: 0.75rem;
		font-family: var(--value-font-primary);
	}

	.error .dialog {
		width: 100%;
		padding: 0.25rem 1rem;
	}

	.error h1 {
		font-size: 2rem;
		margin: 0;
		text-overflow: ellipsis;
		overflow: hidden;
		white-space: pre;
	}

	.error p {
		font-size: 1rem;
		margin: 0;
		margin-top: 0.25rem;
		overflow-x: auto;
	}

	.error a {
		display: block;
		width: 100%;
		padding: 1rem;
		margin-top: 1.25rem;
		text-align: center;
		background: var(--color-tertiary-contaner);
		color: var(--color-on-tertiary-contaner);
		font-weight: bold;
		text-decoration: none;
		border-radius: var(--value-radius);
	}

	@media screen and (min-width: 650px) {
		.center {
			height: 100vh;
		}

		.error {
			min-width: 25em;
			min-height: 12.5em;
			width: auto;
			padding-top: 1rem;
		}
	}
</style>
