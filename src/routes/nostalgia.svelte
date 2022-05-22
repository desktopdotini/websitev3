<script context="module">
	export const prerender = true
</script>

<title>nostalgia</title>

<div class="container">
	<div class="center">
		<div class="error">
			<div class="dialog">
				<h1>nostalgia</h1>
				<br/>
				<audio controls id="nostalgia">
					<source src="./mp3/nostalgia_monv.mp3" type="audio/mpeg">
				  Your browser does not support the audio element.
				</audio> 
			</div>
			<a href="/">Go back home</a>
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
