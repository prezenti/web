<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>


<main>
	<slot />
</main>

<footer>
	<!-- <p>company name....</p> -->
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100vw;
		margin: 0 auto;
		box-sizing: border-box;
		font-family: 'Cormorant Garamond', serif;

	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		position: fixed;
		bottom: 0;
		width:100vw;
		
	}

	footer p {
		font-weight: bold;
		color:var(--tertiary-color);
	}


</style>
